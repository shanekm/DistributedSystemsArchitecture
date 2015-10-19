What is Distrubuted System?
- requires two or more process to function at 100% (if first system fails, other system still continues to work)
- multi-tier application
- Partner level: Exposed interfaces
- Web Scale Services: ie. Facebook connect (identity)
- Useful application that needs to be exposed and used by others

Why build distributed applications?
- Single source of "Truth". ex: how many items I have for sale?
- Enforce uniform rules (documented and undocumented)
- Agility, using same architecture on many other applications (UI for phone, web etc hitting same source)

Components in Distributed Architecture
1. Security
	- Authentication providers maintained centrally
	- Group membershiop maintained in multiple places
	- Authorization distributed
2. Logging, diagnostics
	
3. Data
4. Connectivity

Where components live?
- Internally => my business group, their business group
- Externally => purchased services, free services, partner services

SUMMARY:
1. AmortizationCalculator - calculates payment details based in input
	a. issues - when bug found in calculator new build, new dll and assembly needs to be pushed to users using it (use web service or WCF instead)
		- this allows for one central location of calculator (only one point of entry). All clients using this will see change
		- IAmortize => can be called by clients: Console App, Web App, Loan applicatin etc