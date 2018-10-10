---
title: 'Apéndice A: Proveedores'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbd9536edd15f923af85f2fadad8b696077af4a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485855"
---
# <a name="appendix-a-providers"></a><span data-ttu-id="2206c-102">Apéndice A: Proveedores</span><span class="sxs-lookup"><span data-stu-id="2206c-102">Appendix A: Providers</span></span>


<span data-ttu-id="2206c-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2206c-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2206c-p101">En esta sección se habla sobre tres tipos de proveedores: proveedores de datos, de servicios y componentes de servicios. Los proveedores se clasifican en dos categorías: aquellos que proporcionan datos y aquellos que proporcionan servicios. Un *proveedor de datos* posee sus propios datos y los expone en un formato de tabla en la aplicación del usuario. Un *proveedor de servicios* encapsula un servicio al producir y consumir datos, con lo que aumentan las características de las aplicaciones ADO del usuario. Un proveedor de servicios también puede definirse como un *componente de servicios*, que debe trabajar en cooperación con otros proveedores o componentes de servicios.</span><span class="sxs-lookup"><span data-stu-id="2206c-p101">This section addresses three kinds of providers: data providers, service providers, and service components. Providers fall into two categories: those providing data and those providing services. A *data provider* owns its own data and exposes it in tabular form to your application. A *service provider* encapsulates a service by producing and consuming data, augmenting features in your ADO applications. A service provider may also be further defined as a *service component*, which must work in conjunction with other service providers or components.</span></span>

## <a name="data-providers"></a><span data-ttu-id="2206c-109">Proveedores de datos</span><span class="sxs-lookup"><span data-stu-id="2206c-109">Data Providers</span></span>

<span data-ttu-id="2206c-110">ADO es eficaz y flexible porque puede conectar con varios proveedores de datos distintos y seguir exponiendo el mismo modelo de programación, independientemente de las características específicas de un proveedor concreto.</span><span class="sxs-lookup"><span data-stu-id="2206c-110">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider.</span></span>

<span data-ttu-id="2206c-p102">No obstante, dado que cada proveedor de datos es único, el modo en que la aplicación interactúa con ADO variará ligeramente según el proveedor. Las diferencias suelen clasificarse en tres categorías:</span><span class="sxs-lookup"><span data-stu-id="2206c-p102">However, because each data provider is unique, how your application interacts with ADO will vary slightly by data provider. The differences usually fall into one of three categories:</span></span>

  - <span data-ttu-id="2206c-113">Parámetros de conexión de la propiedad [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2206c-113">Connection parameters in the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

  - <span data-ttu-id="2206c-114">Uso de objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2206c-114">[Command](command-object-ado.md) object usage.</span></span>

  - <span data-ttu-id="2206c-115">Comportamiento del objeto [Recordset](recordset-object-ado.md) del proveedor.</span><span class="sxs-lookup"><span data-stu-id="2206c-115">Provider-specific [Recordset](recordset-object-ado.md) behavior.</span></span>

<span data-ttu-id="2206c-116">A continuación puede ver los detalles de cada uno de los proveedores de datos disponibles en la actualidad desde Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2206c-116">Details for each of the data providers currently available from Microsoft are listed as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2206c-117">Área</span><span class="sxs-lookup"><span data-stu-id="2206c-117">Area</span></span></p></th>
<th><p><span data-ttu-id="2206c-118">Tema</span><span class="sxs-lookup"><span data-stu-id="2206c-118">Topic</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2206c-119">Bases de datos ODBC</span><span class="sxs-lookup"><span data-stu-id="2206c-119">ODBC databases</span></span></p></td>
<td><p><span data-ttu-id="2206c-120"><a href="microsoft-ole-db-provider-for-odbc.md">Proveedor de Microsoft OLE DB para ODBC</a></span><span class="sxs-lookup"><span data-stu-id="2206c-120"><a href="microsoft-ole-db-provider-for-odbc.md">Microsoft OLE DB Provider for ODBC</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2206c-121">Servicios de Index Server de Microsoft</span><span class="sxs-lookup"><span data-stu-id="2206c-121">Microsoft Indexing Service</span></span></p></td>
<td><p><span data-ttu-id="2206c-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Proveedor de Microsoft OLE DB para Servicios de Index Server de Microsoft</a></span><span class="sxs-lookup"><span data-stu-id="2206c-122"><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Microsoft OLE DB Provider for Microsoft Indexing Service</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2206c-123">Servicio de Active Directory de Microsoft</span><span class="sxs-lookup"><span data-stu-id="2206c-123">Microsoft Active Directory Service</span></span></p></td>
<td><p><span data-ttu-id="2206c-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Proveedor de Microsoft OLE DB para Servicio de Active Directory de Microsoft</a></span><span class="sxs-lookup"><span data-stu-id="2206c-124"><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Microsoft OLE DB Provider for Microsoft Active Directory Service</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2206c-125">Bases de datos de Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="2206c-125">Microsoft Jet databases</span></span></p></td>
<td><p><span data-ttu-id="2206c-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Proveedor OLE DB para Microsoft Jet</a></span><span class="sxs-lookup"><span data-stu-id="2206c-126"><a href="microsoft-ole-db-provider-for-microsoft-jet.md">OLE DB Provider for Microsoft Jet</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2206c-127">Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="2206c-127">Microsoft SQL Server</span></span></p></td>
<td><p><span data-ttu-id="2206c-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Proveedor de Microsoft OLE DB para SQL Server</a></span><span class="sxs-lookup"><span data-stu-id="2206c-128"><a href="microsoft-ole-db-provider-for-sql-server.md">Microsoft OLE DB Provider for SQL Server</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2206c-129">Bases de datos de Oracle</span><span class="sxs-lookup"><span data-stu-id="2206c-129">Oracle databases</span></span></p></td>
<td><p><span data-ttu-id="2206c-130"><a href="microsoft-ole-db-provider-for-oracle.md">Proveedor de Microsoft OLE DB para Oracle</a></span><span class="sxs-lookup"><span data-stu-id="2206c-130"><a href="microsoft-ole-db-provider-for-oracle.md">Microsoft OLE DB Provider for Oracle</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2206c-131">Publicación en Internet</span><span class="sxs-lookup"><span data-stu-id="2206c-131">Internet Publishing</span></span></p></td>
<td><p><span data-ttu-id="2206c-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">OLE DB Provider for Internet Publishing</a></span><span class="sxs-lookup"><span data-stu-id="2206c-132"><a href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</a></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a><span data-ttu-id="2206c-133">Propiedades dinámicas específicas de los proveedores</span><span class="sxs-lookup"><span data-stu-id="2206c-133">Provider-Specific Dynamic Properties</span></span>

<span data-ttu-id="2206c-p103">Las colecciones [Properties](properties-collection-ado.md) de los objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) y [Recordset](recordset-object-ado.md) incluyen propiedades dinámicas específicas del proveedor. Estas propiedades ofrecen información acerca de funciones específicas del proveedor distintas a las propiedades integradas admitidas por ADO.</span><span class="sxs-lookup"><span data-stu-id="2206c-p103">The [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), and [Recordset](recordset-object-ado.md) objects include dynamic properties specific to the provider. These properties provide information about functionality specific to the provider beyond the built-in properties that ADO supports.</span></span>

<span data-ttu-id="2206c-p104">Después de establecer la conexión y crear estos objetos, utilice el método [Refresh](refresh-method-ado.md) de la colección **Properties** del objeto para obtener la lista de propiedades específicas del proveedor. Consulte la documentación del proveedor y la Referencia del programador de OLE DB para obtener información detallada acerca de estas propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2206c-p104">After establishing the connection and creating these objects, use the [Refresh](refresh-method-ado.md) method on the object's **Properties** collection to obtain the provider-specific properties. Refer to the provider documentation and the OLE DB Programmer's Reference for detailed information about these dynamic properties.</span></span>

## <a name="service-providers"></a><span data-ttu-id="2206c-138">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2206c-138">Service Providers</span></span>

<span data-ttu-id="2206c-p105">Para utilizar un proveedor de servicios, debe proporcionar una palabra clave. También debe ser consciente de las propiedades dinámicas específicas del proveedor asociadas a cada proveedor de servicios. A continuación se ofrecen detalles sobre los proveedores de servicios disponibles en la actualidad desde Microsoft:</span><span class="sxs-lookup"><span data-stu-id="2206c-p105">To use a service provider, you must supply a keyword. You should also be aware of the provider-specific dynamic properties associated with each service provider. Provider-specific details are listed for each of the service providers currently available from Microsoft:</span></span>

  - [<span data-ttu-id="2206c-142">Servicio de forma de datos de Microsoft para OLE DB</span><span class="sxs-lookup"><span data-stu-id="2206c-142">Microsoft Data Shaping Service for OLE DB</span></span>](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

  - [<span data-ttu-id="2206c-143">Proveedor de persistencia de Microsoft OLE DB</span><span class="sxs-lookup"><span data-stu-id="2206c-143">Microsoft OLE DB Persistence Provider</span></span>](microsoft-ole-db-persistence-provider-ado-service-provider.md)

  - [<span data-ttu-id="2206c-144">Proveedor de servicios remotos de Microsoft OLE DB</span><span class="sxs-lookup"><span data-stu-id="2206c-144">Microsoft OLE DB Remoting Provider</span></span>](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a><span data-ttu-id="2206c-145">Componentes de servicios</span><span class="sxs-lookup"><span data-stu-id="2206c-145">Service Components</span></span>

<span data-ttu-id="2206c-p106">El componente de servicios [Servicio de cursores para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) complementa a las funciones de compatibilidad de cursor de los proveedores de datos. También exige una palabra clave y tiene propiedades dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2206c-p106">The [Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) service component supplements the cursor support functions of data providers. It also requires a keyword and has dynamic properties.</span></span>

<span data-ttu-id="2206c-148">Para obtener más información acerca de los proveedores, vea la documentación de Microsoft OLE DB en el paquete Microsoft Data Access Components SDK o visite el [Centro de desarrollo de plataformas de datos](https://msdn.microsoft.com/data/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="2206c-148">For more information about providers, see the documentation for Microsoft OLE DB in the Microsoft Data Access Components SDK or visit the [Data Platform Developer Center](https://msdn.microsoft.com/data/default.aspx).</span></span>

## <a name="provider-commands"></a><span data-ttu-id="2206c-149">Comandos de proveedor</span><span class="sxs-lookup"><span data-stu-id="2206c-149">Provider Commands</span></span>

<span data-ttu-id="2206c-150">Para cada proveedor enumerado aquí, si las aplicaciones permiten a los usuarios especificar instrucciones SQL como comandos de proveedor, siempre debe validar la entrada del usuario y estar alerta ante ataques posibles intruso mediante instrucciones SQL potencialmente peligrosas, como, como parte de la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="2206c-150">For each provider listed here, if your applications allow users to enter SQL statements as the provider commands, you must always validate the user input and be vigilant of possible hacker attacks using potentially dangerous SQL statement, such as, , as part of the user input.</span></span>
