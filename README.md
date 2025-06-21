# HipFracture
ผู้ป่วยกระดูกสะโพกหัก


## กรองข้อมูลใน diagnosis_opd ที่สนใจ

``` create table hdc_data.temp_l72_opd_set1 as
select distinct t1.hospcode,t1.pid,t1.seq,t1.date_serv,t1.diagtype,t1.diagcode
from diagnosis_opd t1
where t1.diagtype = '1' and t1.diagcode like '%L72%'
```


<dl>diagtype<dl>
  <dt>1. Principle Dx ( โรคหลักที่นำพาผู้ป่วยมาหาเรา)<dt>
  <dt>2. Comorbidity (โรคร่วมที่พบ หรือที่ผู้ป่วยเป็น)<dt>
  <dt>3. Complication (โรคแทรกซ้อน มักเป็นโรคที่เกิดจากผู้ป่วยที่ไป Admit ที่ รพ.)<dt>
  <dt>4. Other (โีรคอื่น ๆ ที่ตรวจพบ แต่ไม่ได้ทำการรักษา)<dt>
  <dt>5. External cause (สาเหตุการเจ็บป่วยภายนอก) <dt>

