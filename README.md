int conta(char s[]){
	
	int i=0;
	
	while(s[i]!='\0'){
		i++;
	}
	return i;
}

int power(int base, int exp){

	int i,ris=1;
	
	for(i=0; i<exp; i++){
		ris*=base;
	}
	return ris;
}


int hex2int(char hex[]) {
	
	int i=0, dim, ris=0, b, esp;

	while (hex[i]!='\0'){
		if(hex[i]>='A' && hex[i]<='F') hex[i]-=7;
		else if (hex[i]>='a' && hex[i]<='f') hex[i]-=39;
		i++;
	}
	
	dim=conta(hex);
	i=dim-1;
	while(i>=0){
		b=(int)((hex[dim-1-i])-48);
		esp=power(16, i);
		ris=ris+(b*esp);
		i--;
	}
	
	return ris;
}
