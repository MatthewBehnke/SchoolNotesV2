#IowaStateUniversity
#ComputerScience 
#COMS362 
#Assignment


---

# [[Classes/ISU/COM S 362/COM S 362]] Module 1 Assignment

[  
COM-S-362-HW1-2022-Spring.pdf](https://canvas.iastate.edu/courses/87069/files/18198724?wrap=1 "COM-S-362-HW1-2022-Spring.pdf") 

Type your answers in a separate document, not hand written.



**

1.  I agree with Fred Books in that there will not be a silver bullet like there was for hardware. The main reasons that I agree there will not be a silver bullet accidental and essential complexity. While software engineers can remove accidental complexity through better management, design, and planning, essential complexity will always be a problem. Currently developing software is a very complex task involving requirements, planning, designing and developing. For each of the steps there just does not exist much if any free space that can be eliminated. Overall I agree with Fred Books and that there will not be a silver bullet for software because there does not exist much free space that can make drastic improvements.
    
2.  A
    

1.  The code does violate the principle of Information hiding
    
2.  The negative impact for violating information hiding is that the user has uncontrolled access to the public Vector variable. Meaning that the user can change it and access it without the IndexedElement class knowing. This can cause problems when there are hidden dependencies that break when uncontrolled access happens. Since the public Vector is being exposed users now depend on it and if we wanted to change it out to something else it would have to get updated everywhere.
    
3.  First the public Vector can be made private and then for every action that the user of the class wants to do can be made into a method. This allows the underlying data structure to be changed and updated without the end user knowing.
    

4.  B
    

1. The code does violate the principle of abstraction

2. First the code is doing more than one thing. It is opening a file, decrypting a file and decompressing a file. In the openFile method it depends on a decryptor and decompressor leading to unwanted dependencies.

3. The code can be updated for the decryptor and decompressor are their own actions outside of the class. The file reader would open the file then onto the file reader a decompressor and a decryptor can be applied. By doing this it solves separation of concerns.

**