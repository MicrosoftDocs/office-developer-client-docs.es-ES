---
title: Objeto de enlace de datos de la Libreta de direcciones
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281870"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="676c5-102">Objeto de enlace de datos de la Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="676c5-102">Address Book Data-Binding object</span></span>


<span data-ttu-id="676c5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="676c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="676c5-p101">La aplicación Libreta de direcciones utiliza el objeto [ RDS.DataControl ](datacontrol-object-rds.md) para enlazar datos de la base de datos de SQL Server a un objeto visual (en este caso, una tabla DHTML) en la página HTML cliente de la aplicación. La lógica del programa VBScript controlada por evento utiliza el objeto [RDS.DataControl](datacontrol-object-rds.md) para:</span><span class="sxs-lookup"><span data-stu-id="676c5-p101">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page. The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="676c5-106">Consultar la base de datos, enviar actualizaciones a la base de datos y actualizar la cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="676c5-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="676c5-107">Permitir a los usuarios desplazarse al registro primero, siguiente, anterior o último en la cuadrícula de datos.</span><span class="sxs-lookup"><span data-stu-id="676c5-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="676c5-108">El código siguiente define el componente **RDS.DataControl**:</span><span class="sxs-lookup"><span data-stu-id="676c5-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="676c5-p102">La etiqueta OBJECT define el componente **RDS.DataControl** en el programa. La etiqueta incluye dos tipos de parámetros:</span><span class="sxs-lookup"><span data-stu-id="676c5-p102">The OBJECT tag defines the **RDS.DataControl** component in the program. The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="676c5-111">Aquéllos asociados con la etiqueta genérica OBJECT.</span><span class="sxs-lookup"><span data-stu-id="676c5-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="676c5-112">Aquéllos específicos del objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="676c5-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="676c5-113">Parámetros genéricos de la etiqueta OBJECT</span><span class="sxs-lookup"><span data-stu-id="676c5-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="676c5-114">En la tabla siguiente, se describen los parámetros asociados con la etiqueta OBJECT.</span><span class="sxs-lookup"><span data-stu-id="676c5-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="676c5-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="676c5-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="676c5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="676c5-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="676c5-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="676c5-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="676c5-p103">Un número único de 128 bits que identifica el tipo de objeto incrustado en el sistema. Este identificador se mantiene en el Registro del sistema del equipo local (para obtener más información de los identificadores de clase del objeto <strong>RDS.DataControl</strong>, vea <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>).</span><span class="sxs-lookup"><span data-stu-id="676c5-p103">A unique, 128-bit number that identifies the type of embedded object to the system. This identifier is maintained in the local computer's system registry. (For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="676c5-121"><strong><em>Id.</em></strong></span><span class="sxs-lookup"><span data-stu-id="676c5-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="676c5-122">Define un identificador del objeto incrustado (válido en todo un documento) que se utiliza para identificarlo en el código.</span><span class="sxs-lookup"><span data-stu-id="676c5-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="676c5-123">Parámetros de etiqueta de RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="676c5-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="676c5-p104">En la tabla siguiente, se describen los parámetros específicos del objeto **RDS.DataControl** (para obtener una lista completa de los parámetros del objeto **RDS.DataControl** y de cuándo implementarlos, vea [RDS.DataControl (objeto)](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="676c5-p104">The following table describes the parameters specific to the **RDS.DataControl** object. (For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="676c5-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="676c5-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="676c5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="676c5-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="676c5-128"><a href="server-property-rds.md">SERVIDOR</a></span><span class="sxs-lookup"><span data-stu-id="676c5-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="676c5-129">Si usa HTTP, el valor es el nombre del equipo servidor precedido por https:// .</span><span class="sxs-lookup"><span data-stu-id="676c5-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="676c5-130"><a href="connect-property-rds.md">CONNECT</a></span><span class="sxs-lookup"><span data-stu-id="676c5-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="676c5-131">Proporciona la información de conexión necesaria para que el objeto <strong>RDS.DataControl</strong> se conecte al servidor SQL Server.</span><span class="sxs-lookup"><span data-stu-id="676c5-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="676c5-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span><span class="sxs-lookup"><span data-stu-id="676c5-132"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="676c5-133">Establece o devuelve la cadena de consulta usada para recuperar el objeto <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="676c5-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

