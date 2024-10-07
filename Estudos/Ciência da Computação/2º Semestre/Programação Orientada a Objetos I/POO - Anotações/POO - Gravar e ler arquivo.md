
### <span style="color:#7317cf">BIBLIOTECAS:</span>

```Java
import java.io.FileWritter;
import java.io.FileReader;
import java.io.IOException;
```

### <span style="color:#7317cf">GRAVAR:</span>

```Java
String varArquivo = "nomeRealdoArquivo.txt"; 

try ( FileWriter writer = new FileWriter(varArquivo)) {
	
	writer.write( "coloca o que será mostrado no arquivo" ) // não necessáriamente precisa estar dentro do writer.write, exemplo: 

	for (int i = 0; i < num; i++) { 
		for (int j = 0; j < num; j++) { 
				writer.write(matriz[i][j] + " "); 
			} 
		} 
		
		System.out.println("Arquivo gravado"); 
		
	} catch (IOException e) { 
		
		System.out.println("Erro ao gravar arquivo" + e.getMessage()); 
}
```

### <span style="color:#7317cf">LER:</span>

```Java 
try ( FileReader fileReader = new FileReader(varArquivo); 
	 
	 Scanner fileScanner = new Scanner(fileReader) ) {
	 
		 while (fileScanner.hasNextLine()) { 
			 String line = fileScanner.nextLine(); 
			 System.out.println(line); 
		} 
		
	} catch (IOException e) { System.out.println("Erro ao ler arquivo" + e.getMessage()); 
```