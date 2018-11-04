---
title: DBEngine.CompactDatabase (método) (DAO)
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
ms.openlocfilehash: df7533376bf6f6d3c5387173a90c7d5e1a5013cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950051"
---
# <a name="dbenginecompactdatabase-method-dao"></a>DBEngine.CompactDatabase (método) (DAO)

**Se aplica a**: Access 2013 | Acceso 2016

Copia y compacta una base de datos cerrada y ofrece la opción de cambiar su versión, de ordenación en orden y el cifrado. (Sólo para áreas de trabajo de Microsoft Access).

> [!NOTE]
> Cuando se usa el cifrado de las tablas vinculadas para acción, actualización y consultas SQL [por ejemplo, una instrucción UPDATE de SQL (CurrentDb.Execute "Actualizar...")], debe proporcionar la clave de cifrado. Además, las tablas vinculadas tienen un límite de 19 caracteres para la clave de cifrado. Vea la sección **Encrypted tablas vinculadas** al final de este tema.

## <a name="syntax"></a>Sintaxis

*expresión* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Opciones***, ***contraseña***)

*expresión* Una expresión que devuelve un objeto **DBEngine** .

## <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Identifica una base de datos existente, cerrado. Puede ser una ruta de acceso completa y el nombre de archivo, como &quot;C:\db1.mdb&quot;. Si el nombre de archivo tiene una extensión, debe especificar. Si la red lo admite, también puede especificar una ruta de acceso de red, tales como &quot; \\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>el nombre de archivo (y la ruta) de la base de datos compactada que está creando. También puede especificar una ruta de acceso de red. No puede usar este argumento para especificar el mismo archivo de base de datos que SrcName.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Expresión de cadena que especifica un orden de intercalación para crear DstName, tal como se ha especificado en los comentarios.</p>
<ul>
<li><p>Si se omite este argumento, la configuración regional de DstName es la misma que SrcName.</p></li>
<li><p>También puede crear una contraseña para DstName concatenando la cadena de contraseña (comenzando por &quot;; pwd =&quot;) con una constante en el argumento DstLocale, como la siguiente: dbLangSpanish &amp; &quot;; pwd = NuevaContraseña&quot;.</p></li>
<li><p>Si desea utilizar el mismo DstLocale que SrcName (el valor predeterminado), pero especificar una nueva contraseña, introduzca simplemente una cadena de contraseña para DstLocale: &quot;; pwd = NuevaContraseña&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Opcional. Constante o combinación de constantes que indican una o varias opciones, tal como se ha especificado en los comentarios. Puede combinar opciones sumando las constantes correspondientes.</p></td>
</tr>
<tr class="odd">
<td><p><em>contraseña</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una expresión de cadena que contiene una clave de cifrado, si se cifra la base de datos. La cadena &quot;; pwd =&quot; deben preceder a la contraseña real. Si incluye una opción de contraseña en DstLocale, este valor se omite.</p><p><strong>Nota</strong>: este es un parámetro en desuso y no se admite en. Formato ACCDB. Para cifrar una. Archivo ACCDB, use la "pwd =" cadena de opción. [!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede utilizar alguna de las constantes siguientes para el argumento DstLocale si desea especificar la propiedad **CollatingOrder** para comparaciones de cadenas de texto.

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
<td><p>Chino simplificado</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Chino tradicional</p></td>
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
<td><p>Sueco y finés</p></td>
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
> Las constantes dbEncrypt dbDecrypt en desuso y no se admite en. Formatos de archivo ACCDB.

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
<td><p>Descifra la base de datos mientras se compacta.</p></td>
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
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0 mientras compacta la base de datos.</p></td>
</tr>
</tbody>
</table>

<br/>

Sólo puede especificar una constante de versión. Si omite una constante de versión, DstName tendrá la misma versión que SrcName. Puede compactar DstName únicamente a una versión que es el mismo o posterior a la de SrcName.

Cuando cambie los datos en una base de datos, el archivo de base de datos puede fragmentarse y utilizar más espacio en disco si es necesario. Puede utilizar el método **CompactDatabase** regularmente para compactar la base de datos y desfragmentar el archivo de base de datos. Las bases de datos compactadas suelen ser más pequeñas y ejecutarse más rápidamente. Puede cambiar también el orden de intercalación, el cifrado o la versión del formato de datos mientras copia y compacta la base de datos.

Debe cerrar SrcName antes de compactarlo. En un entorno multiusuario, otros usuarios no pueden tener abierto SrcName mientras realiza la compactación. Si SrcName no está cerrado o no está disponible para uso exclusivo, se produce un error.

Como **CompactDatabase** crea una copia de la base de datos, debe disponer de espacio en disco suficiente para la base de datos original y duplicada. La operación de compactación producirá un error si no hay espacio en disco suficiente. La base de datos DstName duplicada no tiene que estar en el mismo disco que SrcName. Después de compactar correctamente una base de datos, puede eliminar el archivo SrcName y cambie el nombre del archivo DstName compactado por el nombre del archivo original.

El método **CompactDatabase** copia todos los datos y la configuración de permisos de seguridad de la base de datos especificada por SrcName en la base de datos especificada por DstName.

> [!NOTE]
> [!NOTA] Como el método **CompactDatabase** no convierte los objetos de Microsoft Access, no debe utilizar **CompactDatabase** para convertir una base de datos que contiene estos objetos.

## <a name="encrypted-linked-tables"></a>Cifrar las tablas vinculadas

Las contraseñas cifradas son dependientes en el formato de archivo de la base de datos que va a usar. Si está utilizando un Access 2003 (.mdb) o una base de datos anterior, tendrá una contraseña para proteger la base de datos y una contraseña para cifrar la base de datos independiente. Para Access 2007 (.accdb) y posterior bases de datos (.mdb), la única opción es cifrar y proteger la base de datos con una contraseña, tal y como se ha quitado la opción tener dos contraseñas distintas.

> [!NOTE]
> Para las bases de datos de Access 2007 (.accdb), la contraseña es la clave de cifrado

Puede usar el siguiente ejemplo de código de VBA para un botón de comando:

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

El ejemplo de código siguiente muestra cómo utilizar CompactDatabase con una contraseña (clave de cifrado) y, a continuación, vincular a una tabla en esa base de datos compactada. Tenga en cuenta que se debe proporcionar una contraseña.

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
