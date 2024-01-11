stage ('Deploy CloudFormation Stack') {
    when {
        expression {
            return _action.equals(constants.FULL_BLUE_GREEN) || _action.equals(constants.STAGE)
        }
    }
    steps {
        script {
            // Set the template file path based on your project structure
            def templateFilePath = "/path_to_template/template.json"

            // Set the stack name based on your requirements
            def stackName = "my-new-stack"

            // Set the parameters file path based on your project structure
            def parametersFilePath = "/path_to_parameters/parameters.json"

            // Additional tags as needed
            def tags = "Key1=Value1 Key2=Value2"

            // Construct the deploy command
            def deployCommand = "aws cloudformation deploy" +
                    " --template-file ${templateFilePath}" +
                    " --stack-name ${stackName}" +
                    " --parameter-overrides file://${parametersFilePath}" +
                    " --tags ${tags}"

            // Execute the deploy command
            sh deployCommand
        }
    }
}

