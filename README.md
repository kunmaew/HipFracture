# HipFracture
ผู้ป่วยกระดูกสะโพกหัก


## กรองข้อมูลใน diagnosis_opd ที่สนใจ

> create table hdc_data.temp_l72_opd_set1 as
select distinct 
t1.hospcode,t1.pid,t1.seq,t1.date_serv,t1.diagtype,t1.diagcode
from 
hdc_data.diagnosis_opd t1
where 
t1.diagtype = '1' and t1.diagcode like '%L72%'
