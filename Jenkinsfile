pipeline
{
    agent any
    stages{
        stage ("Build")
        {
            echo "Build Successfully!"
        }
    }
   post
   {
    success
    {
        echo "Completed Successfully!"
    }
    failure
    {
        echo "Deployment failed!"
    }
   }
}