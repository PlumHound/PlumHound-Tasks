![PlumHound](https://raw.githubusercontent.com/DefensiveOrigins/PlumHound/master/docs/images/Plum3.jpg)

# PlumHound-Tasks: Community Marketplace for BloodHoundAD Reporting Engine
## Community Tasks/Work-Plans for PlumHound Report Engine
PlumHound is a Report Engine for the BloodHoundAD graphical database Active Directory tool.  PlumHound-Tasks is a community driven set of tasks (work) that instructs PlumHound to extract specific information from BloodHoundAD and build a subsequent report. 

## Release and call to Action
The initial [PlumHound](https://github.com/DefensiveOrigins/PlumHound) code was released on May 14th, 2020 during a Black Hills Information Security webcast, A Blue Teams Perspective on Red Team Tools.  The webcast was recorded and is available on YouTuve here[Link TBA].

We need PlumHound-Tasks collaborators and maintainers.  If you would like to assist in maintaining the project, please contact the Defensive Origins team through GitHub or Twitter. 

* [Defensive Origins](https://www.defensiveorigins.com)   |  [@DefensiveOGs](https://twitter.com/DefensiveOGs) | [Git](https://github.com/DefensiveOrigins) 
* Kent Ickler  |  @[Krelkci](https://twitter.com/Krelkci) | [Git](https://github.com/Relkci)
* Jordan Drysdale |  [@Rev10D](https://twitter.com/Rev10D) | [Git](https://github.com/rev10d)

<HR>

## Plumhound-Tasks Folder Structure
PlumHound-Tasks repo includes a folder structure to maintain organization of the community provided tasks and report templates.

```plaintext
* tasks: Sets of Tasks 
 -- sets: Task-Lists with multiple job entries
 -- single: Task-Lists with single job entries

* template
 -- CSS: CSS in-line template for report designs
 -- HTML: HTML headers and footers for report design
 -- sets: Sets of HTML headers, footers, and CSS that work together to build a report design
```

<hr>

# TaskLists (ReportEngine Work) 
## TaskList Files Syntax
The PlumHound Repo includes a sample TaskList that exports some basic BloodHoundAD Cypher queries to an HTML Report.  The included tasks\Default.tasks sample shows the basic syntax of the TaskList files.  The TaskList Files allow PlumHound to be fully scripted with batch jobs after the SharpHound dataset has been imported not BloodHoundAD on Neo4j.

### TaskList File Syntax

```plaintext
["Report Title","[Output-Format]","[Output-File]","[CypherQuery]"]
```
<HR>

# Report Templates 
PlumHound allows for the use of HTML markup within its reporting engine.  This includes the ability to add CSS, JavaScript, and other organizational and design markups.  PlumHound-Tasks allows for a venue for community provided templates. 

```plaintext
HTML:
  Options for HTML Output

  --HTMLHeader HTMLHEADER
                        HTML Header (file) of Report
  --HTMLFooter HTMLFOOTER
                        HTML Footer (file) of Report
  --HTMLCSS HTMLCSS     Specify a CSS template for HTML Output
```


 ## CSS Templates
 CSS Template are a method to modify the output design of the PlumHound report engine. PlumHound-tasks provides a venue for community built CSS templates.  
 ```plaintext
python3 PlumHound.py --HTMLCSS ../PlumHound-tasks/template/CSS/example.css -x tasks/default.tasks
```

 ## HTML HEADERS and FOOTERS
 PlumHound also allows for the ingest of HTML headers and footers.  PlumHound-Tasks also is used for a venue for community provided headers and footers that further modify the output of the PlumHounr report engine.
  ```plaintext
python3 PlumHound.py --HTMLHeader ../PlumHound-tasks/template/HTML/example-head.html -x tasks/default.tasks
python3 PlumHound.py --HTMLFooter ../PlumHound-tasks/template/HTML/example-foot.html -x tasks/default.tasks
```

<hr>

## Hat-Tips & Acknowledgements
* See [PlumHound](https://github.com/DefensiveOrigins/PlumHound) for acknowledgments and references. 

## Advisory and Initial Code Contribution
Help PlumHound grow and be a great tool for Blue and Purple Teams.  We've created the initial proof of concept and are committed to continuing the maturity of PlumHound to leverage the power of BloodHoundAD into continual security improvement processes.  Community involvement is what makes this industry great!  
* [Black Hills Information Security](https://www.blackhillsinfosec.com) | [@BHInfoSecurity](https://twitter.com/BHinfoSecurity) | [Discord](https://discord.gg/J4UJPgG)
* [Defensive Origins](https://www.defensiveorigins.com)   |  [@DefensiveOGs](https://twitter.com/DefensiveOGs) | [Git](https://github.com/DefensiveOrigins) 
* Kent Ickler  |  [@Krelkci](https://twitter.com/Krelkci) | [Git](https://github.com/Relkci)
* Jordan Drysdale |  [@Rev10D](https://twitter.com/Rev10D) | [Git](https://github.com/rev10d)


## License
[[GNU GPL3]](https://github.com/DefensiveOrigins/PlumHound-Tasks/blob/master/LICENSE)
