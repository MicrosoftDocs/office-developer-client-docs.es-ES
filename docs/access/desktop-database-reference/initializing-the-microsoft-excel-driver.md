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
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291438"
---
# <a name="initializing-the-microsoft-excel-driver"></a>Inicialización del controlador de Microsoft Excel

**Se aplica a**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office para empresas Access 2013 | Excel 2010 | Access 2010

Al instalar el controlador Excel, el programa de instalación escribe un conjunto de valores predeterminados en el Registro de Windows en las subclaves Engines e ISAM Formats. No es aconsejable modificar estos valores directamente; para ello, utilice el programa de instalación de la aplicación. Las secciones siguientes describen los valores de inicialización y de formato ISAM para el controlador de base de datos de Microsoft Excel.

## <a name="excel-initialization-settings"></a>Excel de inicialización

La carpeta Motores del motor de **\\ conectividad \\ Excel** incluye la configuración de inicialización del controlador Aceexcl.dll, que se usa para el acceso externo a Microsoft Excel hojas de cálculo. En el siguiente ejemplo se muestra una configuración típica para las entradas de esta carpeta.

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
<td><p>win32</p></td>
<td><p>Ubicación de msexcl40.dll. La ruta de acceso completa se determina durante la instalación. Los valores son de tipo REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Número de filas en las que se va a comprobar el tipo de datos. Éste se determina de acuerdo al número máximo de clases de datos que se encuentren. Si no es posible hacerlo de esta manera, se determinará en el siguiente orden: Número, Moneda, Fecha, Texto, Boolean. Si se encuentran datos que no coinciden con el tipo de datos estimado para la columna, se devuelven como un valor <strong>Null</strong>. A la hora de realizar la importación, si una columna tiene tipos de datos mixtos, toda la columna se convertirá de acuerdo con el valor de ImportMixedTypes. El número predeterminado de filas que se van a comprobar es 8. Los valores son de tipo REG_DWORD.</p></td>
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

La carpeta Motores de conectividad **\\ Excel \\ 8.0** contiene las siguientes entradas, que se aplican a Microsoft Excel 97.

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
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exportar datos de la base de datos activa a un archivo de Microsoft Excel 97. Si el archivo de destino ya existe, este proceso sobrescribirá los datos.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Uso de la configuración TypeGuessRows para Excel driver
Al usar Microsoft Excel, puede usar el valor del Registro **TypeGuessRows** para configurar cuántas filas se van a comprobar para el tipo de datos. El **valor TypeGuessRows** se encuentra en la siguiente subclave del Registro:

# <a name="office-2016"></a>[Office 2016](#tab/office-2016)

Para una instalación MSI de Office

- Para las Office de 32 bits en Windows de 32 bits Office de 64 bits en Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Para las extensiones de 32 Office de 64 bits Windows:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
Para una instalación de hacer clic y ejecutar de Office

- Para las Office de 32 bits en Windows de 32 bits Office de 64 bits en Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Para las extensiones de 32 Office de 64 bits Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

El número predeterminado de filas que se deben comprobar es **8** (ocho). Al establecer el valor **TypeGuessRows** en **0** (cero), Excel Driver comprueba las primeras 16 384 filas para el tipo de datos. Si desea comprobar más de 16 384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas que se permiten en Excel).
 
El tipo de datos viene determinado por el número máximo de tipos de datos que se encuentran. Si hay una vinculación, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null. Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**

# <a name="office-2013"></a>[Office 2013](#tab/office-2013)

Para las Office de 32 bits en Windows de 32 bits Office de 64 bits en Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Para las extensiones de 32 Office de 64 bits Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

El número predeterminado de filas que se deben comprobar es **8** (ocho). Al establecer el valor **TypeGuessRows** en **0** (cero), Excel Driver comprueba las primeras 16 384 filas para el tipo de datos. Si desea comprobar más de 16 384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas que se permiten en Excel).
 
El tipo de datos viene determinado por el número máximo de tipos de datos que se encuentran. Si hay una vinculación, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null. Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**

# <a name="office-2010"></a>[Office 2010](#tab/office-2010)

Para las Office de 32 bits en Windows de 32 bits Office de 64 bits en Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Para las extensiones de 32 Office de 64 bits Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

El número predeterminado de filas que se deben comprobar es **8** (ocho). Al establecer el valor **TypeGuessRows** en **0** (cero), Excel Driver comprueba las primeras 16 384 filas para el tipo de datos. Si desea comprobar más de 16 384 filas, establezca **TypeGuessRows** en un valor que se base en el intervalo deseado. Para comprobar todas las filas, establezca **TypeGuessRows** en 1.048.576 (el número máximo de filas que se permiten en Excel).
 
El tipo de datos viene determinado por el número máximo de tipos de datos que se encuentran. Si hay una vinculación, el tipo de datos se determina en el orden siguiente:

- Número
- Moneda
- Fecha
- Texto
- Booleano

Si se encuentran datos que no coinciden con el tipo de datos calculado para la columna, estos datos se devuelven como **un valor** Null. Durante una importación, si una columna tiene tipos de datos mixtos, toda la columna se convierte en el tipo de datos establecido por la configuración **ImportMixedTypes.**

---
> [!NOTE]
> [!NOTA] Si modifica la configuración del Registro de Windows, debe salir y reiniciar el motor de base de datos para que los cambios surtan efecto.

## <a name="see-also"></a>Vea también

- [Uso de la configuración TypeGuessRows para Excel driver](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

