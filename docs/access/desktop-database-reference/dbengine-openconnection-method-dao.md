---
title: Método DBEngine. OpenConnection (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294263"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="9fbf9-102">Método DBEngine. OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="9fbf9-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="9fbf9-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9fbf9-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbf9-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fbf9-104">Syntax</span></span>

<span data-ttu-id="9fbf9-105">*expresión* . OpenConnection (***nombre***, ***Opciones***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="9fbf9-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="9fbf9-106">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9fbf9-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fbf9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="9fbf9-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9fbf9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fbf9-108">Name</span></span></p></th>
<th><p><span data-ttu-id="9fbf9-109">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="9fbf9-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9fbf9-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9fbf9-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="9fbf9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fbf9-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fbf9-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9fbf9-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9fbf9-113">Required</span></span></p></td>
<td><p><span data-ttu-id="9fbf9-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-115">Expresión de cadena.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-115">A string expression.</span></span> <span data-ttu-id="9fbf9-116">Vea la descripción en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbf9-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="9fbf9-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="9fbf9-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="9fbf9-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-p102">Establece varias opciones para la conexión, tal como se especifica en Comentarios. Basándose en este valor, el administrador de controladores ODBC solicita al usuario información de la conexión como el nombre de origen de datos (DSN), el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbf9-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="9fbf9-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="9fbf9-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="9fbf9-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-125"><strong>True</strong> si la conexión se va a abrir para un acceso de sólo lectura y <strong>False</strong>, si se va a abrir para un acceso de lectura/escritura (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="9fbf9-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbf9-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="9fbf9-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="9fbf9-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="9fbf9-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-129">Una cadena de conexión ODBC.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-129">An ODBC connection string.</span></span> <span data-ttu-id="9fbf9-130">Vea la propiedad <strong><a href="connection-connect-property-dao.md">Connect</a></strong> para los elementos y la sintaxis específicos de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="9fbf9-131">Un ODBC &quot;antepuesto; &quot; es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="9fbf9-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fbf9-132">Return value</span></span>

<span data-ttu-id="9fbf9-133">Connection</span><span class="sxs-lookup"><span data-stu-id="9fbf9-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="9fbf9-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9fbf9-134">Remarks</span></span>

<span data-ttu-id="9fbf9-p104">Utilice el método **OpenConnection** para establecer una conexión con un origen de datos ODBC desde un área de trabajo de ODBCDirect. El método **OpenConnection** es similar pero no equivalente a **OpenDatabase**. La diferencia principal es que **OpenConnection** sólo está disponible en un área de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="9fbf9-138">Si especifica un nombre de origen de datos (DSN) ODBC registrado en el argumento Connect, el argumento Name puede ser cualquier cadena válida y también proporcionará la propiedad **Name** para el objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="9fbf9-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="9fbf9-139">Si no se incluye un DSN válido en el argumento Connect, Name debe hacer referencia a un DSN ODBC válido, que también será la propiedad **Name** .</span><span class="sxs-lookup"><span data-stu-id="9fbf9-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="9fbf9-140">Si ni Name ni Connect contienen un DSN válido, se puede establecer el administrador de controladores ODBC (mediante el argumento Options) para solicitar al usuario la información de conexión necesaria.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="9fbf9-141">El DSN suministrado a través de la pregunta proporciona luego la propiedad **Name**.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="9fbf9-142">El argumento Options determina si se debe pedir al usuario que establezca la conexión y cuándo, y si se va a abrir o no la conexión de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="9fbf9-143">Puede utilizar una de las constantes siguientes.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9fbf9-144">Constante</span><span class="sxs-lookup"><span data-stu-id="9fbf9-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="9fbf9-145">Description</span><span class="sxs-lookup"><span data-stu-id="9fbf9-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9fbf9-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-147">El administrador de controladores ODBC utiliza la cadena de conexión proporcionada en <em>dbname</em> y <em>connect</em>.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="9fbf9-148">Si no proporciona suficiente información, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbf9-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-p108">El administrador de controladores ODBC muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>, que indica cualquier información pertinente proporcionada en <em>dbname</em> o <em>connect</em>. La cadena de conexión está constituida por el DSN que el usuario selecciona en los cuadros de diálogo, o, si el usuario no especifica un DSN, se utiliza el DSN predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbf9-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-p109">Opción predeterminada. Si el argumento <em>connect</em> incluye toda la información necesaria para completar una conexión, el administrador de controladores ODBC utiliza la cadena de <em>connect</em>. Si no, se comporta como suele hacerlo cuando especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9fbf9-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-157">Esta opción se comporta igual que <strong>dbDriverComplete</strong> excepto que el controlador ODBC deshabilita las preguntas sobre cualquier información que no sea necesaria para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9fbf9-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="9fbf9-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="9fbf9-159">Ejecuta el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-159">Execute the method asynchronously.</span></span> <span data-ttu-id="9fbf9-160">Esta constante se puede utilizar con cualquiera de las demás constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9fbf9-p111">**OpenConnection** devuelve un objeto **Connection** que contiene información acerca de la conexión. El objeto **Connection** es similar al objeto **[Database](database-object-dao.md)**. La principal diferencia es que el objeto **Database** suele representar una base de datos, aunque también se puede utilizar para representar una conexión con un origen de datos ODBC desde un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

