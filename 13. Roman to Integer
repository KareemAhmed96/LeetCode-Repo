#include <stdio.h>

#define I_Number_Equivalent   1
#define V_Number_Equivalent   5
#define X_Number_Equivalent   10
#define L_Number_Equivalent   50
#define C_Number_Equivalent   100
#define D_Number_Equivalent   500
#define M_Number_Equivalent   1000

int romanToInt(char * s){
    
    char romans;     // Variable to store each roman letter.
    int result = 0;  // Function return variable containing the converted number.
    int counter = 0; // Array index.
    
    while(s[counter] != '\0')
    {   
        romans = s[counter];
    
        switch(romans)
        {
            case 'I':
                // When next roman no. is V (5) or X (10), skip this case.
                if(s[counter+1] == 'V' || s[counter+1] == 'X')
                    break;
                else
                    result += I_Number_Equivalent;
                    
                break;
                
            case 'V':
                result += V_Number_Equivalent;
                if(counter == 0)
                    break;

                // When the previous roman no. was I (1), subtract 1 from the result.
                else if(s[counter-1] == 'I')
                    result -= I_Number_Equivalent;

                break;

            case 'X':
                // When next roman no. is L (50) or C (100), skip this case.
                if(s[counter+1] == 'L' || s[counter+1] == 'C')
                    break;

                if(counter == 0)
                {   
                    result += X_Number_Equivalent;
                    break;
                }
                // When the previous roman no. was I (1), subtract 1 from the result.
                else if(s[counter-1] == 'I')
                    result -= I_Number_Equivalent;

                result += X_Number_Equivalent;

                break;

            case 'L':
                result += L_Number_Equivalent;
                if(counter == 0)
                    break;

                // When the previous roman no. was X (10), subtract 10 from the result.
                else if(s[counter-1] == 'X')
                    result -= X_Number_Equivalent;

                break;

            case 'C':
                // When next roman no. is D (500) or M (1000), skip this case.
                if(s[counter+1] == 'D' || s[counter+1] == 'M')
                    break;

                if(counter == 0)
                {   
                    result += C_Number_Equivalent;
                    break;
                }
                // When the previous roman no. was X (10), subtract 10 from the result.
                else if(s[counter-1] == 'X')
                    result -= X_Number_Equivalent;

                result += C_Number_Equivalent;

                break;

            case 'D':
                result += D_Number_Equivalent;
                if(counter == 0)
                    break;

                // When the previous roman no. was C (100), subtract 100 from the result.
                else if(s[counter-1] == 'C')
                    result -= C_Number_Equivalent;

                break;

            case 'M':
                result += M_Number_Equivalent;
                if(counter == 0)
                    break;

                // When the previous roman no. was C (100), subtract 100 from the result.
                else if(s[counter-1] == 'C')
                    result -= C_Number_Equivalent;
                    
                break;
        }
        counter++;
    }
    return result;
}

int main(void)
{
    char romanNumber[] = "MXCCV";
    int result = romanToInt(romanNumber);

    printf("%d", result);

    return 0;
}
