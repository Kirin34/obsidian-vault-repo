Cosa ho fatto:
		Ho controllato nello standalone.xml cosa ci fosse: I db coincidono con quelli descritti nell'errore.
		Dopodichè sono entrato nel pod, ho controllato che lo standalone.xml fosse presente nel pod e l'ho trovato in /eap/configuration/standalone ed è uguale;
		 Ho lanciato il comando nc -zv ibmpp.allianzit 6029
				Ncat: Connected to ibmpp.allianzit:6029.
				Ncat: 0 bytes sent, 0 bytes received in X.XXX seconds.
		   Ho letto i logs e risultano queste eccezioni: 12:30:10,234 ERROR [org.hibernate.util.JDBCExceptionReporter] (default task-1) javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jdbc/casaDb2DS  
12:30:10,234 WARN  [org.hibernate.cfg.SettingsFactory] (default task-1) Could not obtain connection metadata: java.sql.SQLException: javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jdbc/casaDb2DS  
Caused by: javax.resource.ResourceException: IJ000453: Unable to get managed connection for java:/jdbc/casaDb2DS


Risolto: Central aveva bloccato le utenze.



