	PREDIX APPLICATION

	Technically speaking, we will have two main components in our architecture: Predix Machine & the Predix Application.

	Predix Machine … software components installed on the Raspberry Pi responsible for data capturing and securely streaming into the Predix cloud.  Predix Machine is made of Linux shell scripts, Java programs and  libraries and frameworks provided by Predix, some open source and some copyrighted by GE
	
	Predix Application (App):  a simple front-end on its on web domain to visualize the data captured from the Raspberry Pi.  The App uses three core micro-services to do its job.
	
			§ User Access & Authentication (UAA): part of the Predix catalog, UAA will manage the client control for the connectivity from the Raspberry Pi and the user control for access to the App.
			§ Time series: also part of the Predix catalog, this service is used to efficiently manage, distribute, ingest, and store time series data. Time Series is ideal to manage data from the continuous stream of sensor information since it maintains the arrival time of each stream and index it for faster queries.
			§ Asset: part of the Predix catalog as well, this service is sued to create and store asset models that describe machine types and to instantiate representations of such machines. For our IoT applicaton, the Asset service allows to connect more than one Raspberry Pi or similar device into the same Predix App and manage the different data sources as different assets.
