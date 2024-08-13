# oracle_sample
A Collection of my sample SQL project file


-------------------------SEQUENCE CREATE  and CREATE TABLE --------------------------------------------------------------------------
CREATE SEQUENCE SEQ_TBL_EMP_SUBMISSION 
   INCREMENT BY 1 
   START WITH 1 
   NOCACHE  ORDER  NOCYCLE ;
   
   CREATE SEQUENCE SEQ_SUBMISSION_CODE 
   INCREMENT BY 1 
   START WITH 1
   NOCACHE  ORDER  NOCYCLE  ;

CREATE TABLE TBL_EMP_SUBMISSION(TXID VARCHAR2(50) DEFAULT SYS_GUID(),
                                RID INTEGER DEFAULT (SEQ_TBL_EMP_SUBMISSION.NEXTVAL ),
                              SUBMISSION_CODE NUMBER DEFAULT (SEQ_SUBMISSION_CODE .NEXTVAL ),
                              EMP_CODE VARCHAR2(50),
                              UNIT_CODE NUMBER,
                              DDO_CODE NUMBER,
                              DEPT_CODE NUMBER,
                              SERVICE_RULE_CODE NUMBER,
                              BRANCH_CODE NUMBER,
                              POST_CODE NUMBER,
                              AA_CURRENT_POST_CODE NUMBER,
                              ORG_UNIT_CODE NUMBER,
                              POSITION_CODE NUMBER,
                              WEATHER_EMP_HOLING_FAC VARCHAR2(20),
                              ISACTIVE NUMBER(1,0) DEFAULT 0 CHECK (ISACTIVE IN (0, 1)),
                            INSERTED_ON TIMESTAMP DEFAULT SYSTIMESTAMP,
                            INSERTED_BY VARCHAR2(20) NOT NULL,
                            MODIFIED_ON TIMESTAMP,
                         MODIFIED_BY VARCHAR2(20));
SELECT * FROM TBL_EMP_HOLDING_FAC_SUB;
   CREATE SEQUENCE SEQ_TBL_EMP_HOLDING_FAC_SUB
   INCREMENT BY 1 
   START WITH 1 
   NOCACHE  ORDER  NOCYCLE   ;
   
   CREATE SEQUENCE SEQ_EMP_HOLDING_FAC_SUB_CODE
   INCREMENT BY 1 
   START WITH 1 
   NOCACHE  ORDER  NOCYCLE   ;

 CREATE TABLE TBL_EMP_HOLDING_FAC_SUB(TXID VARCHAR2(50) DEFAULT SYS_GUID(),
                                RID INTEGER DEFAULT (SEQ_TBL_EMP_HOLDING_FAC_SUB.NEXTVAL ),
                              EMP_HOLDING_FAC_SUB_CODE NUMBER DEFAULT (SEQ_EMP_HOLDING_FAC_SUB_CODE .NEXTVAL ),
                              EMP_CODE VARCHAR2(50),
                              DEPT_CODE NUMBER,
                              SERVICE_RULE_CODE NUMBER,
                             BRANCH_CODE NUMBER,
                              POST_CODE NUMBER,
                              AA_CURRENT_POST_CODE NUMBER,
                              ORG_UNIT_CODE NUMBER,
                              POSITION_CODE NUMBER,
                              ISACTIVE NUMBER(1,0) DEFAULT 0 CHECK (ISACTIVE IN (0, 1)),
                            INSERTED_ON TIMESTAMP DEFAULT SYSTIMESTAMP,
                            INSERTED_BY VARCHAR2(20) NOT NULL,
                            MODIFIED_ON TIMESTAMP,
                         MODIFIED_BY VARCHAR2(50));
CREATE SEQUENCE SEQ_TBL_SUB_SR_UPLOAD
   INCREMENT BY 1 
   START WITH 1
   NOCACHE  ORDER  NOCYCLE  ;
   
   CREATE SEQUENCE SEQ_SUB_SR_UPLOAD_CODE 
   INCREMENT BY 1 
   START WITH 1 
   NOCACHE  ORDER  NOCYCLE   ;

 CREATE TABLE TBL_SUB_SR_UPLOAD(TXID VARCHAR2(50) DEFAULT SYS_GUID(),
                                RID INTEGER DEFAULT (SEQ_TBL_SUB_SR_UPLOAD.NEXTVAL ),
                              SUB_SR_UPLOAD_CODE NUMBER DEFAULT (SEQ_SUB_SR_UPLOAD_CODE .NEXTVAL ),
                              EMP_CODE VARCHAR2(50),
                              NUM_SR_PAGS NUMBER,
                              UPLOAD_DOCUMENT  VARCHAR2(250) ,
                              REMARKS VARCHAR2(50), 
                            ISACTIVE NUMBER(1,0) DEFAULT 0 CHECK (ISACTIVE IN (0, 1)),
                            INSERTED_ON TIMESTAMP DEFAULT SYSTIMESTAMP,
                            INSERTED_BY VARCHAR2(20) NOT NULL,
                            MODIFIED_ON TIMESTAMP,
                         MODIFIED_BY VARCHAR2(50));
                         
