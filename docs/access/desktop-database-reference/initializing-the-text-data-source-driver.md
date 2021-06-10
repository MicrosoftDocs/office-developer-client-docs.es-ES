---
title: Inicialización del controlador de origen de datos de texto
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291424"
---
# <a name="initializing-the-text-data-source-driver"></a>Inicialización del controlador de origen de datos de texto

**Se aplica a:** Access 2013, Office 2013

El mismo controlador de base de datos se usa tanto para orígenes de datos de texto como para orígenes de datos HTML.

Al instalar el controlador de base de datos origen de datos de texto, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Microsoft Windows en las subclaves Engines e ISAM Formats. No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación. Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de orígenes de datos de texto.

## <a name="text-data-source-initialization-settings"></a>Configuración de inicialización del origen de datos de texto

La **carpeta De texto \\ ISAM Formats \\ del** motor de conectividad de Access incluye la configuración de inicialización del controlador Acetxt.dll, que se usa para el acceso externo a los archivos de datos de texto. En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Text de la manera siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrada</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Ubicación de Acetxt.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Número de filas que se van a examinar para estimar los tipos de columnas. Si se establece en 0, se analizará el archivo completo. El valor predeterminado es 25. Los valores son de tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila.</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>Indicador de cómo se almacenan las páginas de texto. Los valores válidos son:</p>
<p></p>
<ul>
<li><p>ANSI, la página de códigos ANSI del equipo. Se realizan las conversiones AnsiToUnicode y UnicodeToAnsi.</p></li>
<li><p>OEM, la página de códigos OEM del equipo. Se realizan las conversiones OemToUnicode y UnicodeToOem.</p></li>
<li><p>Unicode, no se realizan las conversiones de página de códigos .</p></li>
<li><p>&lt;número &gt; decimal: el número de página de código de un juego de caracteres específico. Se realizan las conversiones a y desde Unicode.</p></li>
</ul>
<p></p>
<p>El valor predeterminado es ANSI. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>Formato</p></td>
<td><p>Puede ser cualquiera de los siguientes: TabDelimited, CSVDelimited, Delimited ( &lt; single character &gt; ). El delimitador de un solo carácter en el formato Delimitado puede ser cualquier carácter individual excepto una comilla doble ( &quot; ). El valor predeterminado es CSVDelimited. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>Extensiones</p></td>
<td><p>Extensiones de los archivos que se van a examinar al buscar datos basados en texto. Las extensiones predeterminadas son txt, csv, tab, asc. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>Valor binario que indica si se incluye el símbolo de moneda adecuado al exportar campos de moneda. Un valor de 01 indica que se incluye el símbolo. Un valor de 00 indica que sólo se exportan los datos numéricos. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>Formatos ISAM de origen de datos de texto

La **carpeta De texto \\ formatos ISAM \\ del motor** de conectividad de Access contiene las siguientes entradas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Motor</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Archivos de texto (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Archivos de texto (*.txt; *.csv; *.tab; *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importar datos del archivo externo a la base de datos activa. Al cambiar datos en la base de datos activa, no cambiarán los del archivo externo.</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Crear una tabla en la base de datos activa que está vinculada al archivo externo. Si se cambian datos en la base de datos activa, también cambiarán los del archivo externo.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar datos de la base de datos activa a un archivo de texto. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.

## <a name="html-import-isam-formats"></a>Formatos ISAM de importación HTML

La carpeta Importación HTML de **\\ \\ formatos HTML** del motor de conectividad de Access contiene las siguientes entradas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Motor</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Archivos HTML (*.ht*)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Importar datos del archivo externo a la base de datos activa. Al cambiar datos en la base de datos activa, no cambiarán los del archivo externo.</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>Crear una tabla en la base de datos activa que está vinculada al archivo externo. Si se cambian datos en la base de datos activa, también cambiarán los del archivo externo.</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.

## <a name="html-export-isam-formats"></a>Formatos ISAM de exportación HTML

La carpeta Exportación HTML de **\\ isam \\ formatos DE ISAM** del motor de conectividad de Access contiene las siguientes entradas.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de la entrada</p></th>
<th><p>Tipo</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Motor</p></td>
<td><p>REG_SZ</p></td>
<td><p>Texto</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Archivos HTML (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar datos de la base de datos activa a un archivo de texto. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>Personalización del Schema.ini de texto y datos HTML

Para poder leer, importar o exportar texto y datos HTML, es necesario crear un archivo Schema.ini e incluir la información ISAM de texto en dicho archivo. El archivo Schema.ini contiene información detallada sobre un origen de datos: cómo se da formato al archivo de texto, cómo se lee en el momento de la importación y cuál es el formato de exportación predeterminado para los archivos. Los ejemplos siguientes muestran el diseño para un archivo de ancho fijo, Filename.txt:

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

De forma similar, el formato para un archivo delimitado se especifica de la manera siguiente:

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

Si está exportando datos a un archivo de texto delimitado, especifique también el formato de dicho archivo:

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

El ejemplo My Special Export hace referencia a una opción de exportación determinada; es posible especificar cualquier variación de las opciones de exportación a la hora de realizar la conexión. Este último ejemplo también corresponde a un nombre de origen de datos (DSN) que se puede pasar de forma opcional al efectuar la conexión. Se pueden incluir las tres secciones de formato en el mismo archivo .ini.

El motor de base de datos de Microsoft Access utiliza las entradas del archivo Schema.ini de la manera siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Entrada</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>Se puede establecer en <strong>True</strong> (que indica que el primer registro de datos especifica los nombres de las columnas) o en <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Formato</p></td>
<td><p>Se puede establecer en uno de los siguientes valores: TabDelimited, CSVDelimited, Delimited ( &lt; single character ) o &gt; FixedLength. El delimitador especificado para el formato de archivo Delimitado puede ser cualquier carácter único excepto una comilla doble ( &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Sólo se utiliza cuando el formato es FixedLength y se puede establecer en uno de los valores siguientes: RaggedEdge o TrueFixedLength. RaggedEdge permite terminar las filas con un carácter de retorno de carro. TrueFixedLength requiere que cada fila tenga un número exacto de caracteres, y se supone que todos los caracteres de retorno de carro que no están en el límite de la fila están incrustado en un campo. Si este valor no está presente, el valor predeterminado es RaggedEdge.</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>Indica el número de filas que se van a examinar para estimar los tipos de datos de las columnas. Si se establece en 0, se analizará el archivo completo.</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>Se pueden establecer en OEM, ANSI, UNICODE o en el número decimal de una página de códigos válida, e indica el juego de caracteres del archivo de origen.</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>Puede establecerse en una cadena de formato que indica fechas y horas. Esta entrada debe especificarse si durante la importación/exportación todos los campos de fecha y hora se manejan con el mismo formato. Se admiten todos los formatos del motor de base de datos Microsoft Jet, excepto a.m. y p.m. En ausencia de una cadena de formato, se utilizarán las opciones de fecha y hora cortas del Panel de control de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>Indica el símbolo de moneda que se va a utilizar para los valores monetarios en el archivo de texto. Por ejemplo, el signo de dólar ($) y el marco alemán. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>Se puede establecer en cualquiera de los siguientes valores: Prefijo de símbolo de moneda sin separación ($1) Sufijo de símbolo de moneda sin separación (1$) Prefijo de símbolo de moneda con una separación de caracteres ($ 1) Sufijo de símbolo de moneda con una separación de caracteres (1 $) Si esta entrada no está presente, se usa el valor predeterminado en el Panel de control de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>Especifica el número de dígitos utilizado para la parte fraccionaria de una cantidad de moneda. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>Puede ser uno de los siguientes valores: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) El signo de dólar se muestra con fines de este ejemplo, pero debe reemplazarse por el valor currencysymbol apropiado en el programa real. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>Indica el símbolo de carácter único que se va a utilizar como separador de miles para los valores monetarios en el archivo de texto. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>Puede establecerse en cualquier carácter único que se utilice para separar la parte entera de la parte fraccionaria de una cantidad de moneda. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>Puede establecerse en cualquier carácter único que se utilice para separar la parte entera de la fraccionaria de un número. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>Indica el número de dígitos decimales de la parte fraccionaria de un número. Si esta entrada está ausente, se utilizará el valor predeterminado del Panel de control de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>Especifica si un valor decimal menor que 1 y mayor que –1 debe incluir ceros no significativos; este valor puede ser False (no incluir ceros no significativos) o True.</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, ...</p></td>
<td><p>Indica las columnas del archivo de texto que se deben leer. El formato de esta entrada debe ser: <em>Coln</em> = <em>columnName</em> type [Width ] columnName : Los nombres de columna con espacios incrustados deben incluirse entre <em>#</em> comillas. <em></em> <em>tipo</em>: Puede ser Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime. Binary, OLE, Text o Memo. Además, se admiten los siguientes tipos de controladores de texto ODBC: Char (igual que Text) Float (igual que Double) Integer (igual que Short) LongChar (igual que Memo) Formato de fecha Fecha En el caso de un tipo memo, se puede usar un marcador de formato adicional [Hipervínculo de atributo] para especificar columnas que deben ser direcciones URL activas en Microsoft Access. <em></em> En el caso del tipo Decimal, deben utilizarse los marcadores de formato adicionales [Scale #] Precision #].</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>Puede establecerse en cualquier carácter único que se utilice para delimitar cadenas que contengan cualquiera de los demás caracteres especiales. Por ejemplo &quot;abc &quot; , &quot; xyz,pqr , hij Si esta entrada no está presente, el delimitador &quot; predeterminado es una comilla &quot; &quot; doble. Si esta entrada es la cadena ninguno, no se tratará ningún carácter &quot; &quot; como delimitador.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!NOTA] Si modifica la configuración del archivo Schema.ini, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.


