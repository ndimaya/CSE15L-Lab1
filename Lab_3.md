# Lab 3
**Failure**
`There was 1 failure:
arrays first differed at element [0]; expected:<3,2,1> but was:<0>
...(stuff here)
...30 trimmed
caused by: java.lang.AssertionError: expected:<3,2,1> but was:<0>
...(stuff here)
...36 more
Failures!!!
Tests run: 2, Failures: 1`

` static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }`

**Passing**
`JUnit version 4.13.2
..
Time: 0.015

OK (2 tests)`

`static void reverseInPlace(int[] arr) {
    int a = arr[0];
    for (int i = 0, i < arr.length, i += 1) {
        arr[i] = arr[arr.length - i - 1];
        }
    arr[arr.length - 1] = a
    }`

![Image](Lab_3_Code.png)

**Why it Works** The fix works because it copies the original list into a seperate list and then compares the numbers to see which is bigger and makes the list reversed and in proper order.

**Part Two**
source: https://www.redhat.com/sysadmin/linux-find-command

find -iname (approximate name)
`$find ./technical -iname *tech*
home/technical`
`find ./technical -iname *cal*
home/technical`
**Allows for finding apporximate names for files or directories if cant remember exact file.**

find -ls (everything)
`find ./technical -ls
home/technical
home/technical/subtech
home/technical/subtech/subtech`
`find ./technical -ls
home/technical
home/technical/subtechnical
home/technical/subtechnical/subtech`
**Allows for finding of everything that is within a directory.**

find -type
`find ./technical -type f
home/technical/technical.txt`
`find ./technical -type l
home/technical/subtech.org`
**Allows for finding of certain types of files, documents, directories, etc.**

find -maxdepth (limits depth of search)
`find ./technical -maxdepth 1 -iname *tech*
home/technical`
`find ./technical -maxdepth 2 -iname *tech*
home/technical
home/technical/subtechnical`
**Allows for finding of certain files or directories within a certain range.**
