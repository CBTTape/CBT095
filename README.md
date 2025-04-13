# CBT095
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 095 IS FROM MR PAUL G. DAVIS OF EDS IN LOUISVILLE, CO AND *   FILE 095
//*           CONTAINS A COPY OF HIS ISPF EDIT MACROS AND A PROGRAM *   FILE 095
//*           CALLED WHOIS WHICH MAY BE OF INTEREST TO ACF2 USERS   *   FILE 095
//*                                                                 *   FILE 095
//*    EMAIL ADDRESS:    Paul G Davis <miststuck@juno.com>          *   FILE 095
//*                                                                 *   FILE 095
//*   SEE FILE 251 WHICH HAS AN ALMOST ENTIRELY NEW COLLECTION      *   FILE 095
//*   OF PAUL DAVIS' EDIT MACROS.  LOOK BOTH AT THIS FILE AND       *   FILE 095
//*   AT FILE 251 ALSO.                                             *   FILE 095
//*                                                                 *   FILE 095
//*           WHOIS IS A PROGRAM                                    *   FILE 095
//*                                                                 *   FILE 095
//*   EDS AND ENRON CORP IN NO WAY ASSUMES ANY RESPONSIBILITY FOR   *   FILE 095
//*   THE USE OF ANY PART OF THIS CODE.  HOWEVER, IF YOU            *   FILE 095
//*   HAVE ANY QUESTIONS, FEEL FREE TO EMAIL.                       *   FILE 095
//*                                                                 *   FILE 095
//*   With a heavy heart, we regret to mention the passing of       *   FILE 095
//*   Paul Davis on July 19, 2000.  (SG)                            *   FILE 095
//*                                                                 *   FILE 095
//*           THIS FILE IS IN IEBUPDTE SYSIN FORMAT, FOR ADDITIONAL *   FILE 095
//*           INFORMATION PLEASE READ THE MEMBERS THAT START WITH   *   FILE 095
//*           A DOLLAR SIGN ($).  THIS FILE CONTAINS THE FOLLOWING: *   FILE 095
//*                                                                 *   FILE 095
//*           $BASIC        BASIC INSTRUCTIONS FOR USE OF EDIT      *   FILE 095
//*                         MACROS                                  *   FILE 095
//*           $CHANGES      CHANGES AND MODIFICATIONS TO MEMBERS    *   FILE 095
//*           $DESCRPT      DESCRIPTION OF MACROS                   *   FILE 095
//*           $DOC          THIS MEMBER                             *   FILE 095
//*           $SAMPJCL      JCL TO COPY NEEDED MODULES AND COMPILE  *   FILE 095
//*                         LOAD MODULES                            *   FILE 095
//*           $SETUP        SET UP FOR EDIT MACRO USE               *   FILE 095
//*           COBLCAS       COBOL SOURCE FOR LCASE (LOWER CASE)     *   FILE 095
//*                         EDIT MACRO                              *   FILE 095
//*           COBSEPL       COBOL SOURCE FOR SEPLINE EDIT MACRO     *   FILE 095
//*           COBUCAS       COBOL SOURCE FOR UCASE (UPPER CASE)     *   FILE 095
//*                         EDIT MACRO                              *   FILE 095
//*                                                                 *   FILE 095
//*                      $MACROS                                    *   FILE 095
//*                                                                 *   FILE 095
//*           ADDCMDS   CLIST TO ADD ASSIST IN ADDING COMMANDS TO   *   FILE 095
//*                     ISPF COMMAND TABLE                          *   FILE 095
//*           ASMBOX    DRAW A BOX AROUND ASSEMBLY CODE LINES       *   FILE 095
//*                     (COMMENT THEM OUT)                          *   FILE 095
//*           B         BROWSE A MEMBER IN SAME PDS WHEN IN EDIT    *   FILE 095
//*           BIG       CREATE BIG LETTERS IN YOUR TEXT             *   FILE 095
//*           BIGS      CREATE BIG SLANTED LETTERS IN YOUR TEXT     *   FILE 095
//*           BLDCOPY   BUILD IEBCOPY SYSIN STATEMENTS TO COPY      *   FILE 095
//*                     MEMBER OF A PDS                             *   FILE 095
//*           BRODUPDT  NEATLY UPDATE SYS1.BRODCAST MESSAGES        *   FILE 095
//*           CENTER    CENTER TEXT IN YOUR TEXT                    *   FILE 095
//*           CHGALL    QUICK CHANGE ALL COMMAND                    *   FILE 095
//*           CLISTBOX  DRAW A BOX AROUND CLIST LINES (COMMENT THEM *   FILE 095
//*                     OUT)                                        *   FILE 095
//*           CLONE     CLIST TO INVOKE CLONES AND CLONEP FROM ISPF *   FILE 095
//*                     (3.4 ALSO)                                  *   FILE 095
//*           CLONEP    BUILD JCL TO CLONE A PDS                    *   FILE 095
//*           CLONES    BUILD JCL TO CLONE A SEQUENTIAL FILE        *   FILE 095
//*           CMDS      DISPLAY COMMAND TABLE ENTRIES               *   FILE 095
//*           CMDUPDT1  EDIT MACRO CALLED BY ADDCMDS CLIST          *   FILE 095
//*           COBBOX    DRAW A BOX AROUND COBOL CODE LINES (COMMENT *   FILE 095
//*                     THEM OUT)                                   *   FILE 095
//*           COMMENTS  FIND ALL THE COMMENTS IN YOUR DATASET       *   FILE 095
//*           COMPRESS  COMPRESS CURRENT PDS IN PLACE               *   FILE 095
//*           CONLY     CHANGE "ONLY" COMMAND WITH SUB PARAMETERS   *   FILE 095
//*           CONT      PUT CONTINUATION CHARACTER IN COL 72        *   FILE 095
//*           CUSTBOX   DRAW A CUSTOM BOX TO SPECIFICATION LENGTH X *   FILE 095
//*                     WIDTH IN YOUR CODE                          *   FILE 095
//*           CUT       CUT TEXT LINES FROM DATASET TO BE PASTED    *   FILE 095
//*                     LATER                                       *   FILE 095
//*           CUTTO     CUT TEXT LINES FROM DATASET TO ANOTHER      *   FILE 095
//*                     DATASET                                     *   FILE 095
//*           D         DELETE A MEMBER OF THE CURRENT PDS          *   FILE 095
//*           DELCUT    REMOVE A LEVEL OF CUT FROM PROFILE          *   FILE 095
//*           DSIGENP   CREATE IEBCOPY JCL FOR A PDS                *   FILE 095
//*           DSIGENS   CREATE IEBGENER JCL FOR A SEQUENTIAL        *   FILE 095
//*                     DATASET                                     *   FILE 095
//*           E         EDIT ANOTHER MEMBER OF THE CURRENT PDS      *   FILE 095
//*           EDITPDS   CLIST: PERFORM A COMMAND ON ALL MEMBERS OF  *   FILE 095
//*                     A CLIST                                     *   FILE 095
//*           EMACS     LIST TABLE SHOWING EDIT MACRO DESCRIPTIONS  *   FILE 095
//*           FC        FIND PENDING LINE COMMANDS                  *   FILE 095
//*           FIXJCL    TIDY UP YOUR JCL                            *   FILE 095
//*           INIT      INITIAL MACRO FOR EDIT MACRO PURPOSES       *   FILE 095
//*           INITIAL   INITIALIZE DATASET HEADERS FILL IN THE      *   FILE 095
//*                     BLANK INFO                                  *   FILE 095
//*           JC        CREATE A JOBCARD                            *   FILE 095
//*           JCLBOX    DRAW A BOX AROUND JCL LINES (COMMENT THEM   *   FILE 095
//*                     OUT)                                        *   FILE 095
//*           JC2       CREATE A SPECIALIZED JOBCARD                *   FILE 095
//*           JC3       CREATE A JOBCARD WITH REFER INFO            *   FILE 095
//*           JOBCARD   CREATE A JOBCARD                            *   FILE 095
//*           LCASE     CHANGE ENTIRE DATASET TO LOWER CASE         *   FILE 095
//*           LCASEC    CLIST MACRO TO CONVERT A DATASET TO LOWER   *   FILE 095
//*                     CASE                                        *   FILE 095
//*           LJUST     CHANGE AN ENTIRE DATASET TO UPPER CASE      *   FILE 095
//*           MACHELP   GET HELP FOR INDIVIDUAL MACROS              *   FILE 095
//*           MACLIST   DISPLAY A TABLE OF CURRENT ISPF EDIT MACROS *   FILE 095
//*           MEMLIST   SHOW THE MEMBERS IN THE CURRENT PDS         *   FILE 095
//*           MOVECOLS  MOVE COLUMNS OF DATA WITHIN DATASET         *   FILE 095
//*           MRCLEAN   WIPE THE DATA OUT OF MEMBER BUT PRESERVE    *   FILE 095
//*                     THE BLANK LINES                             *   FILE 095
//*           MSTATS    PROVIDE ISPF STATS ON MEMBER WITHOUT        *   FILE 095
//*                     LEAVING EDIT                                *   FILE 095
//*           ONLY      FIND ONLY THE DATA WANTED                   *   FILE 095
//*           OTHER     SAMPLE MACRO TO USE WITH PFSET (CHANGE TO   *   FILE 095
//*                     SUIT NEEDS)                                 *   FILE 095
//*           PARA      WORD PROCESSING POWER FOR ISPF EDIT         *   FILE 095
//*           PARADOC   DOCUMENTATION FOR PARA MACRO                *   FILE 095
//*           PASTE     PASTE DATASET LINE THAT WERE CUT EARLIER    *   FILE 095
//*           PBOX      DRAW A FLOWCHART BOX                        *   FILE 095
//*           PFCAN     RESET PFKEYS BACK TO NORMAL                 *   FILE 095
//*           PFSET     SET PFKEYS TO SPECIAL PURPOSE               *   FILE 095
//*           PRTIT     VPSPRINT CURRENT DATASET                    *   FILE 095
//*           QCREATE   QUICK CREATE TO CURRENT DATASET             *   FILE 095
//*           QREP      QUICK REPLACE TO CURRENT DATASET            *   FILE 095
//*           RCOLDEL   DEL RULE LINES                              *   FILE 095
//*           RCOLS     FANCY RULE                                  *   FILE 095
//*           REPOTHER  QUICK REPLACE TO OTHER DATASET              *   FILE 095
//*           RJUST     RIGHT JUSTIFY TEXT                          *   FILE 095
//*           RNAME     RENAME A MEMBER WHILE IN EDIT               *   FILE 095
//*           S         EDIT A MEMBER OF CURRENT PDS                *   FILE 095
//*           SEPLINE   ADD SEPARATION LINES IN YOUR TEXT           *   FILE 095
//*           SHOWCUT   SHOW TEXT PREVIOUSLY CUT                    *   FILE 095
//*           SHOWCUT2  SHOW ONE LINE OF EACH CUT LEVEL             *   FILE 095
//*           SHOWDCB   SHOW CURRENT DATSET DCB                     *   FILE 095
//*           SHOWFLOW  SHOW THE LOGIC FLOW OF CLIST OR PL/1        *   FILE 095
//*                     PROGRAM                                     *   FILE 095
//*           SHOWMACS  SEE HELP FOR ALL EDITMACS ONE AT A TIME     *   FILE 095
//*           SLINE     PLACE A SINGLE SEPARATION LINE WHERE NEEDED *   FILE 095
//*                     IN TEXT                                     *   FILE 095
//*           SORTDUPS  SORT CURRENT EDIT DATASET AND FIND DUPES    *   FILE 095
//*           ST        SUPERTYPE, TYPE A STRING OF BLOCK LETTERS   *   FILE 095
//*                     NICE....                                    *   FILE 095
//*           STAMP     STAMP DATA INTO YOUR TEXT                   *   FILE 095
//*           STEDITY   EDIT MACRO CALLED BY WHERMEM2               *   FILE 095
//*           STEDIT2   EDIT MACRO CALLED BY WHEREMEM               *   FILE 095
//*           SUM       SUM COLUMNS OF NUMBERS                      *   FILE 095
//*           T         WHAT TIME IS IT                             *   FILE 095
//*           TABLBLD   CLIST: CREATE ISPF TABLE FROM $DESCRPT      *   FILE 095
//*                     MEMBER USED BY EMACS                        *   FILE 095
//*           TYPE      TYPE BLOCK CHARACTERS WITH EASE AND AUTO    *   FILE 095
//*                     SPACING                                     *   FILE 095
//*           TYPESET   EDIT MACRO TO USE WITH PFSET TO SET UP FOR  *   FILE 095
//*                     "TYPE"                                      *   FILE 095
//*           UCASE     CHANGE ENTIRE TEXT TO UPPER CASE            *   FILE 095
//*           UCASEC    CLIST MACRO TO CONVERT A DATASET TO UPPER   *   FILE 095
//*                     CASE                                        *   FILE 095
//*           UNSEP     REMOVE SEPARATION LINES CREATED BY SEPLINE  *   FILE 095
//*           WHEREMEM  CLIST: SHOW OCCURENCE OF MEMBER IN DD       *   FILE 095
//*                     CONCATENATION -- USEFUL                     *   FILE 095
//*           WHERMEM2  CLIST: SAME AS WHEREMEM MORE COMMANDS AND   *   FILE 095
//*                     INFO          -- USEFUL                     *   FILE 095
//*           WIPEIT    ERASE ALL LINES IN DATASET BUT MAINTAIN     *   FILE 095
//*                     BLANK LINES                                 *   FILE 095
//*           XCOPY     COPY A DATASET OTHER THAN THE PDS YOU ARE   *   FILE 095
//*                     WORKING IN                                  *   FILE 095
//*                                                                 *   FILE 095
//*           THESE ARE A COLLECTION OF VARIOUS EDIT MACROS         *   FILE 095
//*           THAT MAY BE SOMEWHAT USEFUL AT YOUR INSTALLATION.     *   FILE 095
//*           SOME OF THEM ARE MY ORIGINAL, AND OTHERS ARE FROM     *   FILE 095
//*           OTHER SHARE USERS.  ALL OF THEM WORK AT THIS SITE.    *   FILE 095
//*           SOME MAY WILL NEED TO BE MODIFIED TO WORK AT YOUR     *   FILE 095
//*           SITE.  TO USE THEM YOU WILL NEED TO HAVE ISPF 2.2 OR  *   FILE 095
//*           LATER AND TSO/E REL 3 OR LATER.                       *   FILE 095
//*                                                                 *   FILE 095
```
