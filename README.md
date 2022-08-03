# Scripttask

// TODO: Add your code here

            string strfileName;//FILENAME ssis variable
            string strfilepath; // FILEPATH ssis variable

            strfilepath = Dts.Variables["User::FILEPATH"].Value.ToString();

            strfileName=Path.GetFileName(strfilepath);
            Dts.Variables["User::FILENAME"].Value = strfileName;

            MessageBox.Show(strfileName);


			Dts.TaskResult = (int)ScriptResults.Success;
      
      
      
