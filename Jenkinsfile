pipeline {

tools{

                 // This section is optional

                // here we write the tools configured that will be used to execute the steps in stages

                     // like maven tool, ansible tool
}


agent {

                // this is a mandatory section
		// In this section we will write labels of the servers where we have to run the pipeline stages
                // By default the pipeline will be executed on the Jenkins server only
                // So the default agent value is always " any "
		// any --> here is any available server --> what is server available right now --> the current Jenkins server
}



/* parameters are used in pipeline to value to all stages
Instead of hard coding the data in the pipeline it is always better to create parameter variables

parameters are nothing but unique names with a value
with a single value or multiple values
parameter can store - String, number, Boolean, choices

As a parameter is used in a pipeline it becomes a parametrized build */

parameters{

String(name: parmName, defaultValue: 'val1' description: 'demo1')
Number
Choice(name: parmName, defaultValue: 'val1' description: 'demo1' choices: ["1","2","3"])
Boolean


}



stages{   // the jobs to be perfomed



stage('Job1')  // Every stage is a independent job
{

    agent {

                label 'testserver'

}
 
   steps{

                       ${params.Name}
            
             // here write steps for what has to be build
}


}

}

}

