# Readers-writers-soln
WRITERS CODE   void  writers{ while(true){ wait(write);  CS  signal(write); } }      READERS CODE   void readers{ while(true){ wait(mutex); readcount++;  if(readcount==1) wait(write); }  signal(mutex);  CS  wait(mutex); readcount--;  if(readcount==0) signal(write); signal(mutex); } }
