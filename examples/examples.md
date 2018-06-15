# examples Commands 
awk '/Jane/' ../testdata/empinfo.txt
awk '{ print $1 }' ../testdata/empinfo.txt
awk '//' ../testdata/empinfo.txt
awk '{ print $1 }' ../testdata/empinfo.txt
awk '{ print }' ../testdata/empinfo.txt 
awk '//{ print }' ../testdata/empinfo.txt
# BEGIN { action / awk-commands }

awk  'BEGIN { print "==Employee Info==" }              # begin block
{ print }                                                # body block
END { print "==ends here==" }'  empinfo.txt              # end block

# awk  'program' input file1 file2 file3 .......file

awk  '{ print }' ../testdata/empinfo.txt /etc/passwd 

# AWK as a filter
awk  '$2==50{ print }'

echo -e "jack \nsam \ntarly \njerry" | awk '/sam/{ print }' 
awk -f ex_cmd.awk ../testdata/empinfo.txt

./ex_comments.awk ../testdata/empinfo.txt
