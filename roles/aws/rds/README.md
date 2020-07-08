# Role: RDS

This role can be used to manage RDS mysql database credentials and grants, primarly developed for use with the Schools Platform.

## Usage

To use these roles, you will have to already setup some form of AWS CLI Credentials either through personal access keys or using
the temporary credentails at runtime <https://ec.awsapps.com/start#/>.

This will then use these credentials to lookup the specified secrets to retrieve the database host, username and password and supply
them to the `mysql_user` ansible module.
