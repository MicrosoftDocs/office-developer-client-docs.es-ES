---
title: Método OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288339"
---
# <a name="openschema-method-ado"></a><span data-ttu-id="f0613-102">Método OpenSchema (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0613-102">OpenSchema method (ADO)</span></span>

<span data-ttu-id="f0613-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0613-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0613-104">Obtiene información del esquema de base de datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0613-104">Obtains database schema information from the provider .</span></span>

## <a name="syntax"></a><span data-ttu-id="f0613-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0613-105">Syntax</span></span>

<span data-ttu-id="f0613-106">**Set\*\*\*recordset*  =  *conexión*. OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span><span class="sxs-lookup"><span data-stu-id="f0613-106">**Set\*\*\*recordset* = *connection*.OpenSchema (* QueryType\*, *Criteria*, *SchemaID*)</span></span>

## <a name="return-values"></a><span data-ttu-id="f0613-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f0613-107">Return values</span></span>

<span data-ttu-id="f0613-108">Devuelve un objeto [Recordset](recordset-object-ado.md) que contiene información de esquema.</span><span class="sxs-lookup"><span data-stu-id="f0613-108">Returns a [Recordset](recordset-object-ado.md) object that contains schema information.</span></span> <span data-ttu-id="f0613-109">El objeto **Recordset** se abrirá como un cursor estático de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f0613-109">The **Recordset** will be opened as a read-only, static cursor .</span></span> <span data-ttu-id="f0613-110">El parámetro *QueryType* determina qué columnas aparecen en el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f0613-110">The *QueryType* determines what columns appear in the **Recordset**.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0613-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0613-111">Parameters</span></span>

|<span data-ttu-id="f0613-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f0613-112">Parameter</span></span>|<span data-ttu-id="f0613-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0613-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f0613-114">*QueryType*</span><span class="sxs-lookup"><span data-stu-id="f0613-114">*QueryType*</span></span> |<span data-ttu-id="f0613-115">Cualquier valor de [SchemaEnum](schemaenum.md) que represente el tipo de consulta de esquema que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="f0613-115">Any [SchemaEnum](schemaenum.md) value that represents the type of schema query to run.</span></span>|
|<span data-ttu-id="f0613-116">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="f0613-116">*Criteria*</span></span> |<span data-ttu-id="f0613-p102">Es opcional. Matriz de restricciones de consulta para cada opción *QueryType*, tal y como se muestra en **SchemaEnum**.</span><span class="sxs-lookup"><span data-stu-id="f0613-p102">Optional. An array of query constraints for each *QueryType* option, as listed in **SchemaEnum**.</span></span>|
|<span data-ttu-id="f0613-119">*SchemaID*</span><span class="sxs-lookup"><span data-stu-id="f0613-119">*SchemaID*</span></span> |<span data-ttu-id="f0613-p103">Identificador GUID de una consulta de esquema del proveedor no definida por la especificación OLE DB. Este parámetro es necesario si el valor de *QueryType* es **adSchemaProviderSpecific**; en caso contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f0613-p103">The GUID for a provider-schema query not defined by the OLE DB specification. This parameter is required if *QueryType* is set to **adSchemaProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f0613-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0613-122">Remarks</span></span>

<span data-ttu-id="f0613-123">El método **OpenSchema** devuelve información autodescriptiva sobre el origen de datos, como qué tablas hay en el origen de datos, las columnas de las tablas y los tipos de datos admitidos.</span><span class="sxs-lookup"><span data-stu-id="f0613-123">The **OpenSchema** method returns self-descriptive information about the data source, such as what tables are in the data source, the columns in the tables, and the data types supported.</span></span>

<span data-ttu-id="f0613-p104">El argumento de *QueryType* es un identificador GUID que indica las columnas devueltas (esquemas). La especificación OLE DB tiene una lista completa de esquemas.</span><span class="sxs-lookup"><span data-stu-id="f0613-p104">The *QueryType* argument is a GUID that indicates the columns (schemas) returned. The OLE DB specification has a full list of schemas.</span></span>

<span data-ttu-id="f0613-p105">El argumento de *Criteria* limita los resultados de una consulta de esquema. *Criteria* especifica una matriz de valores que se deben producir en un subconjunto correspondiente de columnas, denominadas *columnas de restricción*, del objeto **Recordset** resultante.</span><span class="sxs-lookup"><span data-stu-id="f0613-p105">The *Criteria* argument limits the results of a schema query. *Criteria* specifies an array of values that must occur in a corresponding subset of columns, called *constraint columns*, in the resulting **Recordset**.</span></span>

<span data-ttu-id="f0613-p106">La constante **adSchemaProviderSpecific** se utiliza en el argumento de *QueryType* si el proveedor define sus propias consultas de esquema no estándar además de las anteriormente mencionadas. Cuando se utiliza esta constante, el argumento de *SchemaID* debe pasar el identificador GUID de la consulta de esquema que se va a ejecutar. Si el valor de *QueryType* es **adSchemaProviderSpecific** pero no se proporciona *SchemaID*, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="f0613-p106">The constant **adSchemaProviderSpecific** is used for the *QueryType* argument if the provider defines its own nonstandard schema queries outside those listed above. When this constant is used, the *SchemaID* argument is required to pass the GUID of the schema query to execute. If *QueryType* is set to **adSchemaProviderSpecific** but *SchemaID* is not provided, an error will result.</span></span>

<span data-ttu-id="f0613-p107">Los proveedores no tienen que admitir necesariamente todas las consultas de esquema OLE DB estándar. En concreto, la especificación OLE DB sólo requiere **AdSchemaTables**, **adSchemaColumns** y **adSchemaProviderTypes**. Sin embargo, el proveedor no tiene que admitir necesariamente las restricciones de *Criteria* anteriormente mencionadas para esas consultas de esquema.</span><span class="sxs-lookup"><span data-stu-id="f0613-p107">Providers are not required to support all of the OLE DB standard schema queries. Specifically, only **adSchemaTables**, **adSchemaColumns**, and **adSchemaProviderTypes** are required by the OLE DB specification. However, the provider is not required to support the *Criteria* constraints listed above for those schema queries.</span></span>

<span data-ttu-id="f0613-134">**Uso del servicio de datos remotos** El **método OpenSchema** no está disponible en un objeto [Connection del](connection-object-ado.md) lado cliente.</span><span class="sxs-lookup"><span data-stu-id="f0613-134">**Remote Data Service Usage** The **OpenSchema** method is not available on a client-side [Connection](connection-object-ado.md) object.</span></span>

> [!NOTE]
> <span data-ttu-id="f0613-p108">En Visual Basic, las columnas que tienen un entero sin signo de cuatro bytes (DBTYPE UI4) en el objeto **Recordset** devuelto por el método **OpenSchema** en el objeto **Connection**, no se pueden comparar con otras variables. Para obtener más información sobre los tipos de datos OLE DB, vea el capítulo 13 y el apéndice A de la *Referencia del programador de Microsoft OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="f0613-p108">In Visual Basic, columns that have a four-byte unsigned integer (DBTYPE UI4) in the **Recordset** returned from the **OpenSchema** method on the **Connection** object cannot be compared to other variables. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *Microsoft OLE DB Programmer's Reference*.</span></span>


