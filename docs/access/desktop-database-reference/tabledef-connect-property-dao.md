---
title: Propiedad TableDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314388"
---
# <a name="tabledefconnect-property-dao"></a>Propiedad TableDef.Connect (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que proporciona información sobre una tabla vinculada. **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expression* .Connect

*expression* Variable que representa un objeto **TableDef**.

## <a name="remarks"></a>Comentarios

El valor de la propiedad **Connect** es un valor de tipo **String** formado por un especificador de tipo de base de datos y cero o más parámetros separados por puntos y coma. La propiedad **Connect** pasa información adicional a controladores ODBC y algunos controladores ISAM, según sea necesario.

Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de una o dos partes (un especificador de tipo de base de datos y una ruta de acceso a la base de datos), con un punto y coma al final de cada una.

La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=. En algunos casos (como en Microsoft Excel y en la base de datos del motor de bases de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento rutaDeAccesso de la base de datos.

En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de base de datos</p></th>
<th><p>Especificador</p></th>
<th><p>Ejemplo</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Base de datos de Microsoft Access</p></td>
<td><p>[database];</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 o Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS y WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>drive:\path\filename.wk1</p></td>
</tr>
<tr class="odd">
<td><p>Lotus 1-2-3 WK3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>drive:\path\filename.wk3</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WK4</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>drive:\path\filename.wk4</p></td>
</tr>
<tr class="odd">
<td><p>Importación HTML</p></td>
<td><p>HTML Import;</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
<tr class="even">
<td><p>Exportación HTML</p></td>
<td><p>HTML Export;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="odd">
<td><p>Text</p></td>
<td><p>Text;</p></td>
<td><p>drive:\path</p></td>
</tr>
<tr class="even">
<td><p>ODBC</p></td>
<td><p>ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</p></td>
<td><p>Ninguna</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</p></td>
<td><p>drive:\path\filename</p></td>
</tr>
</tbody>
</table>


Si se necesita una contraseña pero ésta no se proporciona en el valor de la propiedad **Connect**, aparecerá un cuadro de diálogo de inicio de sesión la primera vez que el controlador de ODBC tenga acceso a una tabla y aparecerá otra vez si la conexión se cierra y se vuelve a abrir.

Para los datos de Microsoft Exchange, la clave requerida MAPILEVEL debe establecerse en una ruta de acceso de carpeta totalmente resuelta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy"). La ruta de acceso no incluye el nombre de la carpeta que se abrirá como una tabla; en cambio, ese nombre de carpeta debe estar especificado como argumento name para el método **CreateTable**. La clave TABLETYPE debe estar establecida en "0" para abrir una carpeta (forma predeterminada) o en "1" para abrir una libreta de direcciones. La clave PROFILE utiliza como valor predeterminado el perfil que se está utilizando.

Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").

> [!NOTE]
> - Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.
> - Debe tener permisos de acceso al equipo que contiene el servidor de bases de datos al que intenta tener acceso.
