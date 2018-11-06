---
title: DBEngine.CreateDatabase (método) (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9c77eabfc0689c6696c4ea6c8b4998b6b345458
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998353"
---
# <a name="dbenginecreatedatabase-method-dao"></a>DBEngine.CreateDatabase (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Crea un nuevo objeto **[Database](database-object-dao.md)**, guarda la base de datos en disco y devuelve un objeto **Database** abierto (solo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CreateDatabase (***nombre***, ***Configuración regional***, ***opción***)

*expresión* Variable que representa un objeto **DBEngine** .

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
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Cadena de hasta 255 caracteres de longitud que es el nombre del archivo de base de datos que está creando. Puede ser el nombre de archivo y ruta de acceso completo. Si la red lo admite, también puede especificar una ruta de acceso de red, tales como &quot; \\server1\share1\dir1\db1&quot;. Sólo se pueden crear archivos de base de datos de Microsoft Access con este método.</p></td>
</tr>
<tr class="even">
<td><p><em>Configuración regional</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><ul>
<li><p>Expresión de cadena que especifica un orden de intercalación para crear la base de datos, tal como se especifica en la sección de configuración. Debe proporcionar este argumento o se producirá un error.</p></li>
<li><p>También puede crear una contraseña para el nuevo objeto <strong>Database</strong> concatenando la cadena de contraseña (comenzando por &quot;; pwd =&quot; ) con una constante en el argumento de <em>Configuración regional</em> , como la siguiente:</p></li>
<li><p>dbLangSpanish &amp; &quot;; pwd = NuevaContraseña&quot;</p></li>
<li><p>Si desea utilizar el argumento <em>locale</em> predeterminado, pero especificar una contraseña, sólo tiene que agregar una cadena de contraseña al argumento <em>locale</em>:</p></li>
<li><p>&quot;; pwd = NuevaContraseña&quot;</p></li>
<li><p>[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Opción</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante o combinación de constantes que indican una o varias opciones, tal como se especifica en la sección de configuración. Puede combinar opciones sumando las constantes correspondientes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Puede utilizar alguna de las constantes siguientes para el argumento locale si desea especificar la propiedad **[CollatingOrder](database-collatingorder-property-dao.md)** de texto para comparaciones de cadenas.

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


Puede utilizar una o varias de las constantes siguientes en el argumento options para especificar la versión que debe tener el formato de datos y si va a cifrar o no la base de datos.

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
<td><p>Crea una base de datos cifrada.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0.</p></td>
</tr>
</tbody>
</table>


Si omite la constante de cifrado, **CreateDatabase** crea una base de datos no cifrada.

Utilice el método **CreateDatabase** para crear y abrir una nueva base de datos vacía y devolver el objeto **Database**. Debe completar su estructura y contenido con objetos DAO adicionales. Si desea crear una copia parcial o completa de una base de datos existente, puede utilizar el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para crear una copia que pueda personalizar.

