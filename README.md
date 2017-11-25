# SQL
Kurs kodilla

Module 12.3
create table ISSUESLIST
 (
	ID serial primary key,
    NAME varchar(100)
);

create table ISSUESS
(
	ID serial primary key,
    ISSUESLIST_ID bigint unsigned not null,
    SUMMARY varchar(100),
    DESCRIPTION varchar(1025),
    USER_ID_ASSIGNEDTO bigint unsigned not null,
    foreign key(ISSUESLIST_ID) references ISSUESLIST(ID)
);

insert into ISSUESLIST(NAME) value ("In progress");
insert into ISSUESLIST(NAME) value ("ToDo");
insert into ISSUESLIST(NAME) value ("Done");

insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (1,"Study english","I will be learning vocabulary for one hour"); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (1,"Running","I will be running everyday"); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (1,"Study programminig ","I will be learning programming for one hour"); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (1,"Meditaion time","I will be meditate for one hour"); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (1,"Read book","I will be reading book everyday"); 
 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (2,"Study english","I will be learning vocabulary for one hour",7); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (2,"Running","I will be running everyday",4); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (2,"Study programminig ","I will be learning programming for one hour",2); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (2,"Meditaion time","I will be meditate for one hour",2); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (2,"Read book","I will be reading book everyday",3); 

insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (3,"Study english","I will be learning vocabulary for one hour",1); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (3,"Running","I will be running everyday",2); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (3,"Study programminig ","I will be learning programming for one hour",3); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (3,"Meditaion time","I will be meditate for one hour",3); 
insert into ISSUESS(ISSUESLIST_ID, SUMMARY, DESCRIPTION) values (3,"Read book","I will be reading book everyday",2); 

commit;
