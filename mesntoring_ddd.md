"# DDD-Model" 

#Entity:
*Student(Matrikelnummer)
*Mentor
*Organisator
*Person

#Value:
*Termin
*Veranstaltungen

#Services:
*Termine buchen
	Termine.show() zeigt verfügbare Termine an
	Termine.book(Termin t, Student s, Mentor m)	bucht einen freien Termin t
	Termine.export(Person p)	exportiert alle gebuchten Termine einer Person p (Mentor, Student)
	Termine.rematch(Mentor m) 	Termine des Mentors werden auf andere Mentoren umverteilt
	
*Infroamtionen
	Informationen.get(Student s) zeigt alle Informationen zu einem Studenten an
	Informationen.add(Student s)	fügt Informationen hinzu
	
*Veranstaltungen
	Veranstaltung.book(Veranstalung v, Student s) Student belegt Veranstaltung
	Veranstaltugn.delete(Veranstalung v, Student s) Student bricht Veranstaltung ab
	
*Fragebogen
	Fragebogen.send(Student s) sendet Fragebogen an Studen s
