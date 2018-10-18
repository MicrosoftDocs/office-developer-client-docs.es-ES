---
title: DBEngine.OpenConnection Method (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3110bd89b0dc56b13a42c7152465c0f9b39e3175
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607049"
---
# <a name="dbengineopenconnection-method-dao"></a>DBEngine.OpenConnection Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . OpenConnection (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)

*expresión* Variable que representa un objeto **DBEngine** .

### <a name="parameters"></a>Parámetros

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
<td><p>Nombre</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Expresión de cadena. Vea la descripción en Comentarios.</p></td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Establece varias opciones para la conexión, tal como se especifica en Comentarios. Basándose en este valor, el administrador de controladores ODBC solicita al usuario información de la conexión como el nombre de origen de datos (DSN), el nombre de usuario y la contraseña.</p></td>
</tr>
<tr class="odd">
<td><p>ReadOnly</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si la conexión se va a abrir para un acceso de sólo lectura y <strong>False</strong>, si se va a abrir para un acceso de lectura/escritura (opción predeterminada).</p></td>
</tr>
<tr class="even">
<td><p>Conexión</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Una cadena de conexión ODBC. Vea la propiedad <strong><a href="connection-connect-property-dao.md">Connect</a></strong> para los elementos específicos y la sintaxis de esta cadena. Un antepuesto &quot;ODBC; &quot; se requiere.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Valor devuelto
=======
### <a name="return-value"></a>Valor devuelto
>>>>>>> master

Connection

## <a name="remarks"></a>Observaciones

Utilice el método **OpenConnection** para establecer una conexión con un origen de datos ODBC desde un área de trabajo ODBCDirect. El método **OpenConnection** es similar pero no equivalente a **OpenDatabase**. La diferencia principal es que **OpenConnection** sólo está disponible en un área de trabajo ODBCDirect.

Si especifica un nombre de origen de datos (DSN) ODBC registrado en el argumento connect, a continuación, el argumento name puede ser cualquier cadena válida y proporcionará también la propiedad **Name** para el objeto de **conexión** . Si no se ha incluido un DSN válido en el argumento connect, nombre debe hacer referencia a un DSN de ODBC válido, que será también la propiedad **Name** . Si ni name ni connect contienen un DSN válido, se puede establecer el administrador del controlador ODBC (mediante el argumento options) para solicitar al usuario de la información de conexión necesaria. El DSN suministrado a través de la pregunta proporciona luego la propiedad **Name**.

El argumento options determina si se pregunta al usuario que establezca una conexión y cuándo se hace, y si se abre o no la conexión de forma asincrónica. Puede utilizar una de las constantes siguientes.

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
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>El administrador de controladores ODBC utiliza la cadena de conexión proporcionada en <em>dbname</em> y <em>connect</em>. Si no proporciona suficiente información, se produce un error en tiempo de ejecución.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>El administrador de controladores ODBC muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>, que indica cualquier información pertinente proporcionada en <em>dbname</em> o <em>connect</em>. La cadena de conexión está constituida por el DSN que el usuario selecciona en los cuadros de diálogo, o, si el usuario no especifica un DSN, se utiliza el DSN predeterminado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Opción predeterminada. Si el argumento <em>connect</em> incluye toda la información necesaria para completar una conexión, el administrador de controladores ODBC utiliza la cadena de <em>connect</em>. Si no, se comporta como suele hacerlo cuando especifica <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Esta opción se comporta igual que <strong>dbDriverComplete</strong> excepto que el controlador ODBC deshabilita las preguntas sobre cualquier información que no sea necesaria para completar la conexión.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Ejecuta el método de forma asincrónica. Esta constante se puede utilizar con cualquiera de las demás constantes <em>options</em>.</p></td>
</tr>
</tbody>
</table>


**OpenConnection** devuelve un objeto **Connection** que contiene información acerca de la conexión. El objeto **Connection** es similar al objeto **[Database](database-object-dao.md)**. La principal diferencia es que el objeto **Database** suele representar una base de datos, aunque también se puede utilizar para representar una conexión con un origen de datos ODBC desde un área de trabajo de Microsoft Access.

