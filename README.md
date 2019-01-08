Step 1 : Start.

Step 2 : Create SQL Database to Store all the Attributes of the properties through Sql querries.

Step 3 : Declare an variable to store the user information.

         //In this step the user information whether he is buyer or seller of properties is going to be stored.

Step 4 : Check whether the value of variable in Step 3. If it is equal to Seller go to Step 5 or else if it is Buyer go to Step 9.

          if(user=Seller)
           jump to Step 5;
          else
            jump to Step 9; 
            
Step 5 : Declare Variables to Store all the attributes of an property from Seller.

         //In this Step we declare Six Variables to store Id, Lattitude, Longitude, Price, No of Bedrooms, No of Bathrooms.
         
Step 6 : Declare an Variable to Store the property information whether it is for sale or rent.

Step 7 : Store the Data Obtained in Step 5 and Step 6 into SQL Database through Sql querries.

Step 8 : Exit from the Application.

Step 9 : Declare Variables to Store the details of recquirements from buyer.

         //In this step variables are declared to store these recquirements are Id, Lattitude, Longitude, Min Budget, Max Budget, Min                Bedroom recquired, Max Bedroom recquired, Min Bathroom recquired, Max Bathroom recquired.

Step 10 : Declare an Variable to calculate match percent and store the result in that Variable.

Step 11 : Find the Distance of the Property,Declare and Store it in an Variable.

         //1.In this Step Lattitude and Longitude entered by the user are taken and Location should be identified.
         
           2.Then Lattitude and Longitude of all the properties present in Database are taken and location should be identified.
           
           3.Then Diffrence in Miles are calculated and store it in result variable.
           
Step 12 : Perform Validation of Distance Parameter.

           //if(Distance<10)
             return valid;
              else
             return invalid;
             
 Step 13 : Check all constraint and calculate match percent of the Distance parameter and Store result in the variable declared in 
           Step 10.
           
           //Add the match percent value with previous value(In this case zero).
           
 Step 14 : Get the Budget attribute of the Properties From Database and compare with buyer Budget attributes.
 
 Step 15 : Perform Validation of Budget Parameter.
 
           //1.Calculate the 25 percent of user budget and store in variableA
           
             2.Calculate amount by adding value of 25 percent and store in variableB.
             
             3.Calculate amount by subtracting value of 25 percent and store in variableC.
             
               if(Budget>=variableC && Budget<=variableB)
                 return valid;
               else
                 return invalid;
           
 Step 16 : Check all constraint and calculate match percent of the Budget parameter and Store result in the variable declared in 
           Step 10.
           
           //Add the match percent value with previous value(In this case zero).
             Match Percentage is calculated as follows
             
            1.If Both Attributes MinBudget and MaxBudget present 
              if(Budget>=MinBudget && Budget<=MaxBudget)
                Add Full 30 Percentage;
                
            2. If only MinBudget is provided then calculate and Add Full 30 percent if Budget is between +-10% MinBudget or else not.
            
            3. If only MaxBudget is provided then calculate and Add Full 30 percent if Budget is between +-10% MaxBudget or else not.
 
 Step 17 : Get the NoOfBedrooms attribute of the Property From Database and compare with buyer NoOfBedrooms attribute.
 
 Step 18 : Perform Validation of NoOfBedrooms Parameter.
 
            If NoOfBedrooms is between +/- 2
                 return valid;
               else
                 return invalid;
                 
  Step 19 : Check all constraint and calculate match percent of the NoOfBedrooms parameter and Store result in the variable declared             in Step 10.
  
           //Add the match percent value with previous value(In this case zero).
             Match Percentage is calculated as follows
             
            1.If Both Attributes MinBedroomRecquired and MaxBedroomRecquired present 
              if(NoOfBedrooms>=MinBedroomsRecquired && NoOfBedrooms<=MaxBedrooms recquired)
                Add Full 20 Percentage;
                
            2. If only MinBedroomRecquired is provided then calculate match percent according to the value.
            
            3. If only MaxBedroomsRecquired is provided then calculate and match percent according to the value.
                 
 Step 20 :  Get the NoOfBathrooms attribute of the Property From Database and compare with buyer NoOfBathrooms attribute.
 
 Step 21 : Perform Validation of NoOfBathrooms Parameter.
 
            If NoOfBathrooms is between +/- 2
                 return valid;
               else
                 return invalid;
                 
 Step 22 : Check all constraint and calculate match percent of the NoOfBathrooms parameter and Store result in the variable declared             in Step 10.
 
           //Add the match percent value with previous value(In this case zero).
             Match Percentage is calculated as follows
             
            1.If Both Attributes MinBedroomRecquired and MaxBedroomRecquired present 
              if(NoOfBathrooms>=MinBathroomsRecquired && NoOfBathrooms<=MaxBathrooms recquired)
                Add Full 20 Percentage;
                
            2. If only MinBathroomRecquired is provided then calculate match percent according to the value.
            
            3. If only MaxBathroomsRecquired is provided then calculate and match percent according to the value.
            
Step 23 : Jump to Step 9 Untill the end of For loop.

         //Perform for all the properties present in the Database
         
Step 24 : Display all valid Results along with their match Percent and Details os Sale/Rent Information.

           //if(MatchPercent>=40)
              Display Matched property and MatchPercent;
              else
              Display Not Found Message.
      
Step 25 : Stop.             
              
         
