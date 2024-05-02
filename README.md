# URL: https://medium.com/snowflake/snowflake-quick-tips-how-to-use-schemachange-1f578d7882b9

# Set Snowflake password in Terminal variable
export SNOWFLAKE_PASSWORD=Snowflake2021

# Conda ref: https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
conda activate conenv

schemachange -f migrations \
   -a fr55558.eu-central-1 \
   -u runarpersen \
   -r ACCOUNTADMIN \
   -w COMPUTE_WH \
   -d DEMO_DB \
   -c DEMO_DB.SCHEMACHANGE.CHANGE_HISTORY \
   --create-change-history-table