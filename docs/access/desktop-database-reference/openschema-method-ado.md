---
title: OpenSchema (método, ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a204f6e86a1c50be49400430f53dd99468668a9e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950002"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="a3903-102">OpenSchema (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="a3903-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="a3903-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3903-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3903-104">Obtiene información del esquema de base de datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a3903-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="a3903-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3903-105">Syntax</span></span>

<span data-ttu-id="a3903-106">**Establecer \*\*\* recordset* = *conexión*. OpenSchema (* QueryType \*, *criterios*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="a3903-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="a3903-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a3903-107">Return values</span></span>

<span data-ttu-id="a3903-108">Devuelve un objeto [Recordset](recordset-object-ado.md) que contiene información de esquema.</span><span class="sxs-lookup"><span data-stu-id="a3903-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="a3903-109">El objeto **Recordset** se abrirá como un cursor estático de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a3903-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="a3903-110">El *QueryType* determina qué columnas aparecen en el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="a3903-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3903-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3903-111">Parameters</span></span>

|<span data-ttu-id="a3903-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a3903-112">Parameter</span></span>|<span data-ttu-id="a3903-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3903-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a3903-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="a3903-114">*QueryType*</span></span> |<span data-ttu-id="a3903-115">Cualquier valor de [SchemaEnum](schemaenum.md) que represente el tipo de consulta de esquema que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a3903-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="a3903-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="a3903-116">*Criteria*</span></span> |<span data-ttu-id="a3903-117">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="a3903-117">Optional.</span></span> <span data-ttu-id="a3903-118">Una matriz de restricciones de consulta para cada opción *QueryType* , tal y como se muestra en **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="a3903-118">An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="a3903-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="a3903-119">*SchemaID*</span></span> |<span data-ttu-id="a3903-120">Identificador GUID de una consulta de esquema del proveedor no definida por la especificación OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a3903-120">The GUID for a provider-schema query not defined by the OLE DB specification.</span></span> <span data-ttu-id="a3903-121">Este parámetro es necesario si el valor de *QueryType* es **adSchemaProviderSpecific**; de lo contrario, no se usa.</span><span class="sxs-lookup"><span data-stu-id="a3903-121">This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a3903-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3903-122">Remarks</span></span>

<span data-ttu-id="a3903-123">El método **OpenSchema** devuelve información autodescriptiva sobre el origen de datos, como qué tablas hay en el origen de datos, las columnas de las tablas y los tipos de datos admitidos.</span><span class="sxs-lookup"><span data-stu-id="a3903-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="a3903-124">El argumento de *QueryType* es un GUID que indica las columnas devueltas (esquemas).</span><span class="sxs-lookup"><span data-stu-id="a3903-124">The *QueryType* argument is a GUID that indicates the columns (schemas) returned.</span></span> <span data-ttu-id="a3903-125">La especificación OLE DB tiene una lista completa de esquemas.</span><span class="sxs-lookup"><span data-stu-id="a3903-125">The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="a3903-p105">El argumento de *Criteria* limita los resultados de una consulta de esquema. *Criteria* especifica una matriz de valores que se deben producir en un subconjunto correspondiente de columnas, denominadas *columnas de restricción*, del objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="a3903-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="a3903-128">La constante **adSchemaProviderSpecific** se utiliza para el argumento de *QueryType* si el proveedor define sus propias consultas de esquema no estándar fuera de las anteriormente mencionadas.</span><span class="sxs-lookup"><span data-stu-id="a3903-128">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above.</span></span> <span data-ttu-id="a3903-129">Cuando se utiliza esta constante, se requiere el argumento de *SchemaID debe* pasar el identificador GUID de la consulta de esquema para ejecutar.</span><span class="sxs-lookup"><span data-stu-id="a3903-129">When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute.</span></span> <span data-ttu-id="a3903-130">Si *QueryType* es **adSchemaProviderSpecific** pero no se proporciona *SchemaID* , se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="a3903-130">If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="a3903-131">Los proveedores no tienen que admitir necesariamente todas las consultas de esquema OLE DB estándar.</span><span class="sxs-lookup"><span data-stu-id="a3903-131">Providers are not required to support all of the OLE DB standard schema queries.</span></span> <span data-ttu-id="a3903-132">En concreto, la especificación OLE DB sólo requiere **AdSchemaTables**, **adSchemaColumns** y **adSchemaProviderTypes**.</span><span class="sxs-lookup"><span data-stu-id="a3903-132">Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification.</span></span> <span data-ttu-id="a3903-133">Sin embargo, el proveedor no es necesario para admitir las restricciones de *Criteria* mencionadas para esas consultas de esquema.</span><span class="sxs-lookup"><span data-stu-id="a3903-133">However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="a3903-134">**Uso de servicio de datos remotos** El método **OpenSchema** no está disponible en un objeto de [conexión](connection-object-ado.md) de cliente.</span><span class="sxs-lookup"><span data-stu-id="a3903-134">**Remote Data Service Usage**The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a3903-p108">En Visual Basic, las columnas que tienen un entero sin signo de cuatro bytes (DBTYPE UI4) en el objeto <STRONG>Recordset</STRONG> devuelto por el método <STRONG>OpenSchema</STRONG> en el objeto <STRONG>Connection</STRONG>, no se pueden comparar con otras variables. Para obtener más información sobre los tipos de datos OLE DB, vea el capítulo 13 y el apéndice A de la <EM>Referencia del programador de Microsoft OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="a3903-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the <STRONG>Recordset</STRONG> returned from the <STRONG>OpenSchema</STRONG> method on the <STRONG>Connection</STRONG> object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the <EM>Microsoft OLE DB Programmer's Reference</EM>.</span></span></P>


