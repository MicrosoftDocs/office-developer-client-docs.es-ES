---
title: DBEngine.OpenConnection (método) (DAO)
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
ms.openlocfilehash: f958081ee73e64ca6c895217c8aa3e821617b283
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927196"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="3ed22-102">DBEngine.OpenConnection (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ed22-102">DBEngine.OpenConnection method (DAO)</span></span>


<span data-ttu-id="3ed22-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ed22-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed22-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ed22-104">Syntax</span></span>

<span data-ttu-id="3ed22-105">*expresión* . OpenConnection (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)</span><span class="sxs-lookup"><span data-stu-id="3ed22-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="3ed22-106">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="3ed22-106">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="3ed22-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ed22-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ed22-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ed22-108">Name</span></span></p></th>
<th><p><span data-ttu-id="3ed22-109">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="3ed22-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3ed22-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3ed22-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="3ed22-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ed22-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ed22-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ed22-112">Name</span></span></p></td>
<td><p><span data-ttu-id="3ed22-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3ed22-113">Required</span></span></p></td>
<td><p><span data-ttu-id="3ed22-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p101">Expresión de cadena. Vea la descripción en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ed22-117">Options</span><span class="sxs-lookup"><span data-stu-id="3ed22-117">Options</span></span></p></td>
<td><p><span data-ttu-id="3ed22-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="3ed22-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="3ed22-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p102">Establece varias opciones para la conexión, tal como se especifica en Comentarios. Basándose en este valor, el administrador de controladores ODBC solicita al usuario información de la conexión como el nombre de origen de datos (DSN), el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ed22-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3ed22-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="3ed22-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="3ed22-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="3ed22-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-125"><strong>True</strong> si la conexión se va a abrir para un acceso de sólo lectura y <strong>False</strong>, si se va a abrir para un acceso de lectura/escritura (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="3ed22-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ed22-126">Conexión</span><span class="sxs-lookup"><span data-stu-id="3ed22-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="3ed22-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="3ed22-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="3ed22-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-129">Una cadena de conexión ODBC.</span><span class="sxs-lookup"><span data-stu-id="3ed22-129">An ODBC connection string.</span></span> <span data-ttu-id="3ed22-130">Vea la propiedad <strong><a href="connection-connect-property-dao.md">Connect</a></strong> para los elementos específicos y la sintaxis de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="3ed22-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="3ed22-131">Un antepuesto &quot;ODBC; &quot; se requiere.</span><span class="sxs-lookup"><span data-stu-id="3ed22-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3ed22-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ed22-132">Return value</span></span>

<span data-ttu-id="3ed22-133">Connection</span><span class="sxs-lookup"><span data-stu-id="3ed22-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed22-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ed22-134">Remarks</span></span>

<span data-ttu-id="3ed22-p104">Utilice el método **OpenConnection** para establecer una conexión con un origen de datos ODBC desde un área de trabajo ODBCDirect. El método **OpenConnection** es similar pero no equivalente a **OpenDatabase**. La diferencia principal es que **OpenConnection** sólo está disponible en un área de trabajo ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="3ed22-138">Si especifica un nombre de origen de datos (DSN) ODBC registrado en el argumento connect, a continuación, el argumento name puede ser cualquier cadena válida y proporcionará también la propiedad **Name** para el objeto de **conexión** .</span><span class="sxs-lookup"><span data-stu-id="3ed22-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="3ed22-139">Si no se ha incluido un DSN válido en el argumento connect, nombre debe hacer referencia a un DSN de ODBC válido, que será también la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="3ed22-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="3ed22-140">Si ni name ni connect contienen un DSN válido, se puede establecer el administrador del controlador ODBC (mediante el argumento options) para solicitar al usuario de la información de conexión necesaria.</span><span class="sxs-lookup"><span data-stu-id="3ed22-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="3ed22-141">El DSN suministrado a través de la pregunta proporciona luego la propiedad **Name**.</span><span class="sxs-lookup"><span data-stu-id="3ed22-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="3ed22-p106">El argumento options determina si se pregunta al usuario que establezca una conexión y cuándo se hace, y si se abre o no la conexión de forma asincrónica. Puede utilizar una de las constantes siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ed22-144">Constante</span><span class="sxs-lookup"><span data-stu-id="3ed22-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="3ed22-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ed22-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ed22-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p107">El administrador de controladores ODBC utiliza la cadena de conexión proporcionada en <em>dbname</em> y <em>connect</em>. Si no proporciona suficiente información, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ed22-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p108">El administrador de controladores ODBC muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>, que indica cualquier información pertinente proporcionada en <em>dbname</em> o <em>connect</em>. La cadena de conexión está constituida por el DSN que el usuario selecciona en los cuadros de diálogo, o, si el usuario no especifica un DSN, se utiliza el DSN predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ed22-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p109">Opción predeterminada. Si el argumento <em>connect</em> incluye toda la información necesaria para completar una conexión, el administrador de controladores ODBC utiliza la cadena de <em>connect</em>. Si no, se comporta como suele hacerlo cuando especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ed22-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-157">Esta opción se comporta igual que <strong>dbDriverComplete</strong> excepto que el controlador ODBC deshabilita las preguntas sobre cualquier información que no sea necesaria para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="3ed22-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ed22-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="3ed22-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="3ed22-p110">Ejecuta el método de forma asincrónica. Esta constante se puede utilizar con cualquiera de las demás constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p110">Execute the method asynchronously. This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3ed22-p111">**OpenConnection** devuelve un objeto **Connection** que contiene información acerca de la conexión. El objeto **Connection** es similar al objeto **[Database](database-object-dao.md)**. La principal diferencia es que el objeto **Database** suele representar una base de datos, aunque también se puede utilizar para representar una conexión con un origen de datos ODBC desde un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ed22-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

