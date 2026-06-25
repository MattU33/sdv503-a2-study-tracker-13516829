// studyTracker_pseudocode
// -----------------------------------------------------------------------------
// GLOBAL STORAGE
// -----------------------------------------------------------------------------
Initialize a public list called studySessions to store recorded session objects


// -----------------------------------------------------------------------------
// INPUT VALIDATION FUNCTIONS
// -----------------------------------------------------------------------------

Function isValidTopic(givenText):
    If givenText is empty, missing, or only spaces:
        Return False
    Otherwise:
        Return True


Function isValidMinutes(givenText):
    If givenText is empty or missing:
        Return False
        
    Convert givenText to a number
    
    If the text isn't a valid number, or it has decimals, or it is 0 or negative:
        Return False
    Otherwise:
        Return True


// -----------------------------------------------------------------------------
// CALCULATIONS & DISPLAY FUNCTIONS
// -----------------------------------------------------------------------------

Function calculateTotalMinutes():
    Set total to 0
    For each session in studySessions:
        Add the session's minutes to total
    Return total


Function displaySessionsList():
    Print banner headers for "HISTORICAL STUDY SESSIONS"
    
    If studySessions is empty:
        Print "No study sessions recorded yet."
    Otherwise:
        For each session in studySessions (keep track of the row number):
            Print "[Row Number] Topic: [Session Topic] | Duration: [Session Minutes] mins"
        
        Call calculateTotalMinutes() to get the sum
        Print "TOTAL TIME ELAPSED: [Sum] minutes"


// -----------------------------------------------------------------------------
// MAIN CONTROL LOOP APPLICATION
// -----------------------------------------------------------------------------

Function startTrackerApp():
    Set appIsRunning to True
    
    While appIsRunning is True:
        Print the Main Menu choices:
            1. Log a New Session
            2. List All Recorded Sessions
            3. Close Application
            
        Ask user for their option and strip out extra spaces
        
        ------------------------------------------------------------------------
        CASE 1: User chooses Option "1" (Log Session)
        ------------------------------------------------------------------------
        Ask user for the study topic name
        If the topic fails isValidTopic():
            Print error message
            Jump back to the start of the menu loop (continue)
            
        Ask user for the duration in whole minutes
        If the minutes fail isValidMinutes():
            Print error message
            Jump back to the start of the menu loop (continue)
            
        Convert the validated minutes text into an actual integer
        Clean up any leading/trailing spaces from the topic name
        
        Create a new session record containing the clean topic and integer minutes
        Add this new record to the studySessions list
        Print a success message to the user
        
        ------------------------------------------------------------------------
        CASE 2: User chooses Option "2" (View History)
        ------------------------------------------------------------------------
        Call displaySessionsList()
        
        ------------------------------------------------------------------------
        CASE 3: User chooses Option "3" (Exit)
        ------------------------------------------------------------------------
        Print a friendly goodbye message
        Set appIsRunning to False to break the loop
        
        ------------------------------------------------------------------------
        CASE 4: Anything else
        ------------------------------------------------------------------------
        Print an error message for an invalid selection

// EXECUTION ENTRY POINT
Call startTrackerApp()