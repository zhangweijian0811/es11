int sottostringa(char s[], char sub[]) {
	
	int i=0, j=0, pos=0, set=0, quit=0;
	
	while(sub[j]!='\0'&& quit==0){
		if(s[i]=='\0') quit=1;
		if(s[i]==sub[j]){
			if(set==0) pos=i;
			set=1;
			j++;
		}
		else { 
			if(set==1) i--;
			set=0; 
			pos=-1;
			j=0;
		}
		i++;
	}	
	return pos;
}
