# java-list-disk-swap
Java list implementation that swaps data pages to disk in order to use less RAM

The intention of this implementation is to manage a huge data size that exceeds available RAM 
without the need to use a database or files.

This solution uses a Java List implementation that only uses a smaller portion of RAM by swapping data to disk.
Yes, it uses a file to store pages of data; but it is done behind the scene. 
The idea is that a java developer will be able to use this implementation as an ArrayList.

The reason I am implementing this is for my own amusement and I think might be practical for some solution out there.

Usage example:

  
       DataSwapperList dsl = new DataSwapperList();
    
       DataSwapperList dsl = new DataSwapperList(PAGE_SIZE);

       DataSwapperList dsl = new DataSwapperList(PAGE_SIZE, "/tmp/dsl");




