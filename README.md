Virtual Fitness Trainer
                  
                        Description
 
    The Flex Core Gym is a fitness and wellness center. The management has decided to compute a virtual personalized fitness score for each session based on the exercise type, repetitions, and duration. As a programmer, help the trainer evaluate these sessions effectively.
    Functional Requirements:
    
        
            
                Req. #
                Requirements Description
                 Type (Class)
                Method Name
                Parameters 
                Responsibilities
            
        
        
            
                1.
                Extract the details of the workout session and create an object for the WorkoutSession class.
                 WorkoutUtility 
                extractSessionDetails
                String sessionDetails
                This method accepts workout session details as a colon-separated string in the format (sessionId:exerciseType:reps:duration). It parses the values, validates them, and returns a populated WorkoutSession object.
            
            
                2.
                Calculate the fitness score of the workout.
                 WorkoutSession
                calculateFitnessScore  
                 
                This method calculates and returns the fitness score of a workout session. The fitness score is calculated by multiplying the number of repetitions (reps) by the duration of the workout in minutes (duration) and by an intensity factor that depends on the type of exercise performed.The intensityFactor is determined based on the exerciseType of the session, using the following mapping:
                    
                        
                            
                                Exercise Type(case-sensitive)
                                Intensity Factor
                            
                        
                        
                            
                                pushup
                                1.2
                            
                            
                                squat
                                1.0
                            
                            
                                plank
                                1.5
                            
                            
                                burpee
                                1.8
                            
                          
                                Unkown excercise type
                                0.5
                            


                        
                    Constraints:
                        
                    
                        The calculated fitness score should be returned as double.If the duration is less than 10, return -1 and terminate.
                    


                
            
        
    
    
    You are provided with the main method in the UserInterface class as code template, and it is excluded from evaluation.



    
    Note:
    
        Edit only the WorkoutSession and WorkoutUtility classes to implement the business requirements.
        The methods and the constructor should be public, and the attributes of the class should be private.
        In the Sample Input / Output provided, the highlighted text in bold corresponds to the input given by the user and the rest of the text represents the output.
        Ensure that the names for classes, attributes, and methods are provided as specified in the question description.
        Please do not use System.exit(0); to terminate the program.
    
        
        Input Format:  <sessionId>:<exerciseType>:<reps>:<duration>
        
        
            Sample Input / Output 1  
                Enter workout details: 
                S1234:plank:30:20
                Workout Summary:
                Session Id : S1234
                Exercise Type : plank
                Reps : 30
                Duration (min) : 20
                Fitness Score : 900.00
                
              
            
                Sample Input / Output 2
                 
                    Enter workout details: 
                    S1245:Aerobic:30:8
                    Invalid session details
