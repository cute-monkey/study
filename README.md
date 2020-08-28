# study
int findString(char** words, int wordsSize, char* s){
    int i=0,j=0;
    for(i;i<wordsSize;i++){
        j=strcmp(words[i],s);
        if(j==0){
            break;
        }
    }
    if(j!=0){
        return -1;
    }else{
        return i;
    }

    
}
