#Name: Ken Deng
#Major: Computer Science
#Date: 04/15/2015
name=input("Hi, what is your name?")
print("Hello "+name+"! Let's play a game!\nThink of random number from 1 to 100, and I'll try to guess it!")
playGame='yes'	#playGame is the loop condition
while(playGame=='yes'):
	maxNum=101
	minNum=0
	count=0
	f=50	#f is the middle value
	print("Is it ",f,"?")
	a=input("yes/no\n")	#a is to judge if the number is the right one
	count=count+1
	while(a=='no'):
		count=count+1
		c=input("Is the number larger than "+str((maxNum+minNum)//2)+"? yes/no\n")	#c is to judge if the value is larger than the right number
		if(c=='yes'):
			minNum=(minNum+maxNum)//2	
		else:
			maxNum=(minNum+maxNum)//2
		f=(maxNum+minNum)//2
		print("Is it ",f,"?")
		a=input("yes/no\n")
	print("Yeey! I got it in "+str(count)+" tries!")
	playGame=input("Do you want to play more? yes/no\n")
print("Bye-bye")	#say goodbye immediately when you jump out the loop
