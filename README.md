# Oracle

--Usage of TYPE in Oracle

declare
--type usage
	Type v_listTables IS TABLE OF CNTL_DATA.***%ROWTYPE;
	  temp v_listTables;
	  v_list1 v_listTables;
	  v_list2 v_listTables;
	  v_list3 v_listTables;
begin


v_list1:= temp;
				select ****(column name) into vname from ****(table name) where ****;
				DBMS_OUTPUT.PUT_LINE( 'vname: '||vname);
				SELECT SEGMENT_EMT_DEF_REF_ID ,SEGMENT_LIBRARY_ID ,SEGMENT_SUBSEGMENT_NAME ,VERSION ,IS_ACTIVE ,CREATED_BY ,CREATED_DATE      ,MODIFIED_BY ,MODIFIED_DATE ,SEGMENT_SUBSEGMENT_SHORT_NAME ,LVL_NUMBER BULK COLLECT
				  INTO v_list1
				  FROM CNTL_DATA.SEGMENT_EMT_DEF_REF ref;
		
          FOR varR IN v_list1.first..v_list1.last LOOP
          
            DBMS_OUTPUT.PUT_LINE( v_list1(varR).SEGMENT_SUBSEGMENT_NAME);
            
          END LOOP;
end;
