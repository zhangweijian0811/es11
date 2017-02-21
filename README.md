int conta(char s[]) {
	int i=0;
	while (s[i]!='\0')	{
		i++;
	}
	return i;
}
int palindroma(char s[]) {
	int i, j, dim;
	if (s[0] != '\0')
		dim = conta(s);
		i = 0;
		j = dim - 1;
		while (i < dim) {
			if (s[i] != s[j]) {
				if (i != dim - 1) {
					while (i<(dim-1))
					{
						i++;
						j--;
					}
					printf("0\n");
					return 0;
				}
			}
			else while (s[i] == s[j])
			{
				i++;
				j--;
				if (i = (dim - 1)) {
					printf("1\n");
					return 1;
				}
			}
			i++;
			j--; 
		}
	if (s[0] == '\0') {
			printf("1\n");
			return 1;
		}
	return -1;
}
