---
title: Método DBEngine.CompactDatabase (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294340"
---
# <a name="dbenginecompactdatabase-method-dao"></a>Método DBEngine.CompactDatabase (DAO)

**Se aplica a:** Access 2013 | Access 2016

Copia y compacta una base de datos cerrada, y permite cambiar su versión, el orden de intercalación y el cifrado. (Solo áreas de trabajo de Microsoft Access).

> [!NOTE]
> Al usar tablas vinculadas cifradas para consultas de acción, actualización y SQL [como una instrucción SQL UPDATE (CurrentDb.Execute "UPDATE...")], debe proporcionar la clave de cifrado. Además, las tablas vinculadas tienen un límite de 19 caracteres para la clave de cifrado. Consulte la sección **Tablas vinculadas cifradas** al final de este tema.

## <a name="syntax"></a>Sintaxis

*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)

*expression* Expresión que devuelve un objeto **DBEngine**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Identifica una base de datos existente y cerrada. Puede ser una ruta de acceso completa y el nombre del archivo, como &quot;C:\db1.mdb&quot;. Si el nombre de archivo tiene una extensión, debe especificarla. Si la red lo admite, puede especificar también una ruta de red, como &quot;\\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nombre de archivo (y la ruta) de la base de datos compactada que va a crear. Puede especificar también una ruta de red. No puede utilizar este argumento para especificar el mismo archivo de base de datos que SrcName.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expresión de cadena que especifica un orden de intercalación para crear DstName, como se especifica en Comentarios.</p>
<ul>
<li><p>Si omite este argumento, la configuración regional de DstName es la misma que la de SrcName.</p></li>
<li><p>Puede crear también una contraseña para DstName concatenando la cadena de contraseña (que empieza por &quot;;pwd=&quot;) con una constante en el argumento DstLocale, como la siguiente: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</p></li>
<li><p>Si quiere utilizar el mismo DstLocale que SrcName (el valor predeterminado), pero especificar una nueva contraseña, solo tiene que especificar una cadena de contraseña para DstLocale: &quot;;pwd=NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Opcional. Constante o combinación de constantes que indican una o varias opciones, tal como se ha especificado en los comentarios. Puede combinar opciones sumando las constantes correspondientes.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expresión de cadena que contiene una clave de cifrado, si la base de datos está cifrada. La cadena &quot;;pwd=&quot; debe preceder a la contraseña real. Si incluye una opción de contraseña en DstLocale, se omite esta configuración.</p><p><strong>NOTA</strong>: este es un parámetro en desuso y no es compatible con el formato .ACCDB. Para cifrar un archivo .ACCDB, use la cadena de opción "pwd =". Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. En las contraseñas no seguras estos elementos no se combinan. Contraseña segura: Y6dh!et5. Contraseña no segura: Casa27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede usar una de las siguientes constantes para el argumento DstLocale para especificar la propiedad **CollatingOrder** para comparaciones de cadenas de texto.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Orden de intercalación</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Árabe</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>chino simplificado</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>chino tradicional</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Ruso</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Checo</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Neerlandés</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Griego</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Hebreo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Húngaro</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Islandés</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Japonés</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Coreano</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Noruego y danés</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Polaco</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Esloveno</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Español (alfab. tradicional)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Sueco y finlandés</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Tailandés</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Turco</p></td>
</tr>
</tbody>
</table>

<br/>

Puede utilizar alguna de las constantes siguientes en el argumento options para especificar si va a cifrar o descifrar la base de datos mientras se compacta.

> [!NOTE]
> La constantes dbEncrypt y dbDecrypt están en desuso y no se admiten en formatos de archivo .ACCDB.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Cifra la base de datos mientras se compacta.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>Descifrar la base de datos mientras se compacta.</p></td>
</tr>
</tbody>
</table>

<br/>

Si omite una constante de cifrado o si incluye **dbDecrypt** y **dbEncrypt**, DstName tendrá el mismo cifrado que SrcName.

Puede utilizar alguna de las constantes siguientes en el argumento options para especificar la versión del formato de datos de la base de datos compactada. Esta constante afecta únicamente a la versión del formato de datos de DstName y no a la versión de los objetos definidos por Microsoft Access, como formularios o informes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0 mientras compacta la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1 mientras compacta la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0 mientras compacta la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5) mientras compacta la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0 mientras compacta la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Crea una base de datos que usa el formato de archivo de motor de base de datos Microsoft Access versión 12.0 mientras se compacta.</p></td>
</tr>
</tbody>
</table>

<br/>

Solo puede especificar una constante de versión. Si se omite, DstName tendrá la misma versión que SrcName. Sólo puede compactar DstName en una versión que sea la misma o superior a la de SrcName.

Cuando cambie los datos en una base de datos, el archivo de base de datos puede fragmentarse y utilizar más espacio en disco si es necesario. Puede utilizar el método **CompactDatabase** regularmente para compactar la base de datos y desfragmentar el archivo de base de datos. Las bases de datos compactadas suelen ser más pequeñas y ejecutarse más rápidamente. Puede cambiar también el orden de intercalación, el cifrado o la versión del formato de datos mientras copia y compacta la base de datos.

Debe cerrar SrcName antes de compactarla. En un entorno multiusuario, otros usuarios no pueden tener abierto SrcName mientras realiza la compactación. Si SrcName no está cerrado o no está disponible para uso exclusivo, se produce un error.

Como **CompactDatabase** crea una copia de la base de datos, debe disponer de espacio en disco suficiente para la base de datos original y duplicada. La operación de compactación producirá un error si no hay espacio en disco suficiente. La base de datos DstName duplicada no tiene que estar en el mismo disco que SrcName. Una vez compactada correctamente la base de datos, puede eliminar el archivo SrcName y cambiar el nombre del archivo DstName compactado por el nombre de archivo original.

El método **CompactDatabase** copia todos los datos y la configuración de permisos de seguridad de la base de datos especificada por SrcName en la base de datos especificada por DstName.

> [!NOTE]
> Como el método **CompactDatabase** no convierte los objetos de Microsoft Access, no debería usar **CompactDatabase** para convertir una base de datos que contiene esos objetos.

## <a name="encrypted-linked-tables"></a>Tablas vinculadas cifradas

Las contraseñas con cifrado dependen del formato de archivo de la base de datos que está usando. Si usa una base de datos de Access 2003 (.mdb) o anterior, tendrá una contraseña para proteger la base de datos y una contraseña independiente para cifrar la base de datos. En las bases de datos de Access 2007 (.accdb) y posteriores (.mdb), la única opción es cifrar y proteger la base de datos con una contraseña, ya que se ha quitado la opción de las dos contraseñas independientes.

> [!NOTE]
> En bases de datos de Access 2007 (.accdb), la contraseña es la clave de cifrado.

Puede usar el siguiente ejemplo de código VBA para un botón de comando:

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

El ejemplo siguiente muestra cómo usar CompactDatabase con una contraseña (clave de cifrado) y, después, vincularla a una tabla de esa base de datos compactada. Tenga en cuenta que debe proporcionar una contraseña.

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
