bool isPalindrome(int x){
    
    int i = 0;
    int temp;
    char string[100];
    
    if(x < 0)
        return 0;
    
    while(x != 0)
    {
        temp = x % 10;
        
        string[i] = temp;
        
        x /= 10;
        i++;
    }
    
    for(int counter = 0 ; counter < i ; counter++)
    {
        if(string[counter] == string[i-1])
        {
            i--;
        }
        else
        {
            return 0;
        }
    }
    return 1;
}

