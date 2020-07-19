Cloud storage  :
-Storage classes
 - Requester Pays: billing config consumer need to changeges
-Object life cycle
   storage class object apply
   gsutil rewrite -s [STORAGE_CLASS] gs://[PATH_TO_OBJECT]
Where:
[STORAGE_CLASS] is the new storage class for your object. For example, nearline.
[PATH_TO_OBJECT] is the name of the object whose class you want to change. For example, pets/dog.png. 
-Object meta data - cache max age 
-Composte object - large size devide , upload object comine  
gsutil compose gs://src1 gs://src2 
-MAX size of object in bucket - 5 TB
-Resumebeluploads - large size upload if fails retry again
POST /bucker/?uploadType=resumeable
-API codes:
https://cloud.google.com/storage/docs/json_api/v1/status-codes 
-Stram data - dash option with piple line 
https://www.qwiklabs.com/focuses/2765?parent=catalog
-Version of objects - accedent delete object can retry ,gsutil versioning set on " gs:///" 
-Custom meta data -color:red remain on only new uploaded object if object update it reset to 1 , 2 versions 
-Life cycle versioning - policy contins one more rule(s) - objects should match affect , single object can match 2 rules , *delete operation precidance then other *,nearline or coldline then it will moveto coldline -smart decision taker ,
lifecycle- rule[action,condation], action delete , condiation age and isAlive=True and versions objects the a[[;ly to real object if isAlive=False then archive objects deleted, gsutil lifecycle set POLICY.JSON bucketNAME
#setStorageClass - lifecyle.rule.action.type-setStoageClass,stoageClass,Condiation.age,matchSotageClass

-StackDriver
-free debug,error,profile , free till quota -50 GB per project ,Traces 20 millisons, monitoring rest apsi class nbasex
-Workspace configure -muli project single project configure , aws account external confiute, alter ,uptime chekc ,debug ,trace
-Grups -logical groups -filter match , 6 max , region application 
-Dashboard -pane of glass , chats -mtrics ,chart ,stanard or agent metics , metrics/ resourece
metric/resource - TYPEs 
-Alter policy - metric threadpolicy ,incident -ACK,RESLOVE,comment

Alert >> Incident >> Acked or resolved >>. Email send 
Create policy/viewpolicy

-UPTIME check 
http URL for resourece ,path probe intervel

-Monitoring Agents - install using shell for custom metics
APP engine and GKE default avalibale
-LOGGING - any log can use , filter ,analysis ,export 
Logs based metics 

_Logviewr -per projects , export and filer 
filter -resources type ,log level, log type -activity and viiity_log filter 
-Export -Synch -*bigquery,storage,pub sub*

_LOG MATRICS- SYStem and user define matics (400 erro count)

-AUDIT logs

Admin activity - resouce modfiy and meta and configs 
System events - migratios ,backup ,snapshot logs
Data acess Logs -create/modify/ user data ,privatte ;pgs

-ACTIVIty logs 
Diffreent from stackdriver - Creae dataset ,by user name ,create vm ,update vm

-RENTSION
 SYSTEM/ADMIN-400 days
DATA -40 days
-ERROR REPORTING 
Single dashbaord -go ,Ruby,.net ,log api ,dedicate report api
RETENSION =30 days









