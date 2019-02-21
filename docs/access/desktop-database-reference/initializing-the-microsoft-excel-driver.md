---
title: Inicialización del controlador de Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cec7890385e5730831cea9241278511d88b6f3a1
ms.sourcegitcommit: 8ead5b5501f59c108cf02969070be21f7fc52467
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2019
ms.locfileid: "30135750"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Inicialización del controlador de Microsoft Excel

**Se aplica a**: Access 2013 | Office 2013

Cuando se instala el controlador de Excel, el programa de instalación escribe un conjunto de valores predeterminados en el registro de Windows, en las subclaves de los motores y los formatos ISAM. No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación. Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.

## <a name="excel-initialization-settings"></a>Configuración de inicialización de Excel

La carpeta de **Excel\\motores\\del motor de conectividad de Access** incluye la configuración de inicialización del controlador Aceexcl. dll, que se usa para el acceso externo a las hojas de cálculo de Microsoft Excel. En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

El motor de base de datos de Microsoft Access utiliza las entradas de la carpeta Excel de la manera siguiente.

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
<td><p>Win32</p></td>
<td><p>Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Número de filas que se va a comprobar el tipo de datos. El tipo de datos se determina según el número máximo de tipos de datos encontrados. Si hay una empate, el tipo de datos se determina en el siguiente orden: número, moneda, fecha, texto, booleano. Si se encuentran datos que no coinciden con el tipo de datos adivinado para la columna, se devuelve como un valor <strong>nulo</strong> . En la importación, si una columna tiene tipos de datos mezclados, se convertirá toda la columna de acuerdo con la configuración ImportMixedTypes. El número predeterminado de filas que se va a comprobar es 8. Los valores son de tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Su valor se puede establecer en MajorityType o Text. Si se establece en MajorityType, las columnas con tipos de datos mixtos se convertirán al tipo de datos predominante en la importación. Si se establece como Text, las columnas con tipos de datos mixtos se convertirán a texto en la importación. El valor predeterminado es Text. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Número de filas en blanco que se deben agregar al final de una hoja de cálculo de la Versión 3.5 o 4.0 antes de que se agreguen nuevos datos. Por ejemplo, si se establece AppendBlankRows en 4, Microsoft Jet agregará 4 filas en blanco al final de la hoja de cálculo antes de agregar filas que contengan datos. Los valores enteros para esta configuración pueden oscilar entre 0 y 16; el valor predeterminado es 01 (se agrega una fila adicional). Los valores son de tipo REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Valor binario que indica si la primera fila de la tabla contiene nombres de columna. Un valor de 01 indica que, durante la importación, los nombres de columna se toman de la primera fila. Un valor de 00 indica que no hay nombres de columna en la primera fila; dichos nombres aparecerán como F1, F2, F3, etc. El valor predeterminado es 01. Los valores son de tipo REG_BINARY.</p></td>
</tr>
</tbody>
</table>

<br/>

La carpeta **Excel 8,0\\de\\los motores del motor de conectividad de Access** contiene las siguientes entradas, que se aplican a Microsoft Excel 97.

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
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>4,00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>4,00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
</tbody>
</table>

## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Uso de la configuración TypeGuessRows para el controlador de Excel
Cuando se usa un controlador de Microsoft Excel, se puede usar el valor del registro **TypeGuessRows** para configurar el número de filas que se van a comprobar para el tipo de datos. El valor **TypeGuessRows** se encuentra en la siguiente subclave del registro:

# <a name="office-2016taboffice-2016"></a>[Office 2016](#tab/office-2016)

Para una instalación MSI de Office

- Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**

- Para Office de 32 bits en Windows de 64 bits:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**
    
Para una instalación de hacer clic y ejecutar de Office

- Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**

- Para Office de 32 bits en Windows de 64 bits:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access conectividad de Engine\Engines\Excel**

El número predeterminado de filas que se va a comprobar es **8** (ocho). Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos. Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).
 
El tipo de datos se determina por el número máximo de tipos de datos que se encuentra. Si hay una empate, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** . Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .

# <a name="office-2013taboffice-2013"></a>[Office 2013](#tab/office-2013)

Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**

Para Office de 32 bits en Windows de 64 bits:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**

El número predeterminado de filas que se va a comprobar es **8** (ocho). Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos. Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).
 
El tipo de datos se determina por el número máximo de tipos de datos que se encuentra. Si hay una empate, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** . Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .

# <a name="office-2010taboffice-2010"></a>[Office 2010](#tab/office-2010)

Para Office de 32 bits en Windows de 32 bits o Office de 64 bits en Windows de 64 bits:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**

Para Office de 32 bits en Windows de 64 bits:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access conectividad de Engine\Engines\Excel**

El número predeterminado de filas que se va a comprobar es **8** (ocho). Cuando se establece el valor **TypeGuessRows** en **0** (cero), el controlador de Excel comprueba las primeras 16.384 filas para el tipo de datos. Si desea comprobar más de 16.384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas permitidas en Excel).
 
El tipo de datos se determina por el número máximo de tipos de datos que se encuentra. Si hay una empate, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos adivinados para la columna, esos datos se devuelven como un valor **nulo** . Durante una importación, si una columna tiene tipos de datos mezclados, toda la columna se convierte en el tipo de datos que establece la configuración **ImportMixedTypes** .

---
> [!NOTE]
> [!NOTA] Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.

## <a name="see-also"></a>Vea también

- [Uso de la configuración TypeGuessRows para el controlador de Excel](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
