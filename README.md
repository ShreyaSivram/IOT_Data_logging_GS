<img width="1262" alt="image" src="https://github.com/user-attachments/assets/4f94b355-74de-4312-9288-1002dc7354af" /># IOT_Data_logging_GS
This project leverages the ESP32 microcontroller and Google Sheets for real-time data logging of environmental parameters. Utilizing a BME280 sensor, the system continuously measures temperature, humidity, and pressure. These readings are transmitted to a Google Sheets spreadsheet, enabling remote monitoring and data analysis. The project employs Wi-Fi connectivity for internet access and utilizes the ESP-Google-Sheet-Client library for seamless integration with Google Sheets. The system includes features for automatic time synchronization via NTP and secure authentication using Google Service Account credentials. This setup provides a robust and efficient solution for IoT-based environmental data logging and cloud storage.

1. Go to Google Cloud Console.
2. Create a new project or choose an existing project. We’ll show you how to create a new project.
3. Give a name to your project. Then, click Create.
4. Now, you need to create a service account for that project. At the left sidebar, click on Service accounts and then, click on + Create Service Account.
5. Insert a name for your Service account, then click Create and Continue.
6. Select the service account role. Select Owner. Then, click Continue.
7. Finally, DONE.
8. Select the project, click on the three dots icon, and then click on Manage Keys.

Then, create a new key. 
Then, select JSON and click Create.
Copy the project_id, client_email, private_key_id and private_key from the .json file because you’ll need them later.
Click on the following link: https://console.cloud.google.com/apis/library/sheets.googleapis.com and enable Google Sheets API 
In the Arduino IDE, go to Sketch > Library > Manage Libraries. Search for ESP-Google-Sheet-Client and click Install.

Go to Google Sheets and create a new spreadsheet. Give a title to your spreadsheet. For example ESP32 Datalogging.
Save the spreadsheet ID. It’s highlighted in the picture in the last slide.
At the top right corner click on Share. Paste the service account email and click Send.
After uploading the code to the ESP32, open the Serial Monitor to check the process.
The ESP32 should successfully connect to your Wi-Fi network and after 30 seconds, it should publish its first reading.
Open the spreadsheet where you’re publishing the values. You should see new values being published in real-time. The first column contains the epoch time, then the temperature in Celsius degrees, the humidity, and finally the pressure in hPa.








