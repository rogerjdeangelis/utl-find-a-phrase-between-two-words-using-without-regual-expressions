# utl-find-a-phrase-between-two-words-using-without-regual-expressions
Find a phrase between two words using without regual expressions 
    Find a phrase between two words using without regual expressions                                              
                                                                                                                  
    github                                                                                                        
    https://tinyurl.com/y378kmot                                                                                  
    https://github.com/rogerjdeangelis/utl-find-a-phrase-between-two-words-using-without-regual-expressions       
                                                                                                                  
    SAS Forum                                                                                                     
    https://tinyurl.com/y56txy53                                                                                  
    https://communities.sas.com/t5/SAS-Programming/find-a-phrase-between-two-words-using-RE/m-p/557401            
                                                                                                                  
                                                                                                                  
    The op wanted to use regular expression, however that suloutin is Klingon code.                               
                                                                                                                  
     Problem                                                                                                      
                                                                                                                  
            After This            Extract                           After                  Extract                
             =========            ==========                        ======               ============             
        test reporting: by Jones 'left home' was inform: home found Tasks: provide about 'left home8'             
                                                                                                                  
    *_                   _                                                                                        
    (_)_ __  _ __  _   _| |_                                                                                      
    | | '_ \| '_ \| | | | __|                                                                                     
    | | | | | |_) | |_| | |_                                                                                      
    |_|_| |_| .__/ \__,_|\__|                                                                                     
            |_|                                                                                                   
    ;                                                                                                             
                                                                                                                  
    cards4;                                                                                                       
    test reporting: by Jones 'left home' was inform: home found Tasks: provide about 'left home8'                 
    ;;;;                                                                                                          
    run;quit;                                                                                                     
                                                                                                                  
    *            _               _                                                                                
      ___  _   _| |_ _ __  _   _| |_                                                                              
     / _ \| | | | __| '_ \| | | | __|                                                                             
    | (_) | |_| | |_| |_) | |_| | |_                                                                              
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                             
                    |_|                                                                                           
    ;                                                                                                             
                                                                                                                  
    Up to 40 obs from WANT total obs=1                                                                            
                                                                                                                  
    Obs    LEFTHOME1    LEFTHOME2                                                                                 
                                                                                                                  
     1     left home    left home8                                                                                
                                                                                                                  
    *                                                                                                             
     _ __  _ __ ___   ___ ___  ___ ___                                                                            
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                           
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                           
    | .__/|_|  \___/ \___\___||___/___/                                                                           
    |_|                                                                                                           
    ;                                                                                                             
                                                                                                                  
    data want;                                                                                                    
      infile cards4 delimiter="'";                                                                                
      informat lefthome1 lefthome2 $10.;                                                                          
      input                                                                                                       
            @'reporting'  @"'" lefthome1                                                                          
            @'Tasks'      @"'" lefthome2;                                                                         
    cards4;                                                                                                       
    test reporting: by Jones 'left home' was inform: home found Tasks: provide about 'left home8'                 
    ;;;;                                                                                                          
    run;quit;                                                                                                     
                                                                                                                  
                                                                                                                  
