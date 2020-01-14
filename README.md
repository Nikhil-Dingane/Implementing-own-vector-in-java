# Introduction to vector : 
   A vector is a type of dynamic array, which grows according to its need. We can access the vector elements using an integer index. We can insert the element in between the vector, which is not possible in case of an array.
   A vector, in programming, is a type of array that is one dimensional. Vectors are a logical element in programming languages that are used for storing data. Vectors are similar to arrays but their actual implementation and operation differ.
    

**A vector in java :**
    The Vector class implements a growable array of objects. Like an array, it contains components that can be accessed using an integer index. However, the size of a Vector can grow or shrink as needed to accommodate adding and removing items after the Vector has been created. 

How will I implement own vector in java:
    I will take the reference of the Vector class which is already present in Java. I am taking the reference of that class and I will try to implement same the class manually, which will act as original vector class.

**The design approach of the vector class:**
    I am going to design the vector class according to the Vector class already present in the java. This class contains three characteristics(data members) as an array of Object class, the number of actual elements in a vector and capacity of incrementation of the vector. They will be as follows:
    #
    
	class Vector
	{
        protected Object[] elementData;
        protected int elementCount;
        protected int capacityIncreament;
	
  	//methods
  	public MyVector()                                                   
  	public MyVector(int initialCapacity)                 
	public MyVector(int initialCapacity,int capacityIncrement)     
	public void addElement(T obj) 
	public boolean removeElement(T obj)
	public void add(T obj)
	public add(int index, T obj)
	public boolean remove(int index)
	public void display()
	public void removeAllElements()
	public int capacity()
	public void clear()
	public int size()
	public boolean contains(T obj)
	public Object elementAt()
	public void ensureCapacity()
	public Object firstElement()
	public Object LastElement()
	public Object get(int index)
	public void set(int index,T obj)
	public boolean isEmpty()
	public int indexOf(T obj)
}

**How will I manage the memory when the vector grows:**
	Before inserting the element in the vector I should sure that the vector has sufficient memory or not. If it has no memory then I  will allocate the new memory to the array of Object class. This memory allocation will be based on the value stored in the capacityIncreament.
If the value is 0 then the size of the newly allocated memory will be double the current size of the array of Object class and if it is greater than 0 then the size of new memory allocation will be the current size of the  array elementData + capacityIncreament.
    
