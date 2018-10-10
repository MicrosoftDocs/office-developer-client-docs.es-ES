---
title: Utilizar ADO con ADO MD
TOCTitle: Using ADO with ADO MD
ms:assetid: 93d1d270-b8d0-4489-d441-11a61887291c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249655(v=office.15)
ms:contentKeyID: 48546405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492efdcef5f71daf50ac84eec5e61ef4ed07fd5a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485186"
---
# <a name="using-ado-with-ado-md"></a><span data-ttu-id="57c45-102">Utilizar ADO con ADO MD</span><span class="sxs-lookup"><span data-stu-id="57c45-102">Using ADO with ADO MD</span></span>


<span data-ttu-id="57c45-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="57c45-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="57c45-p101">ADO y ADO MD son modelos de objetos relacionados pero independientes. ADO proporciona objetos para conectarse a orígenes de datos, ejecutar comandos, recuperar datos tabulares y metadatos de esquema en formato de tabla, y ver información de errores del proveedor. ADO MD proporciona objetos para recuperar datos multidimensionales y ver metadatos de esquema multidimensional.</span><span class="sxs-lookup"><span data-stu-id="57c45-p101">ADO and ADO MD are related but separate object models. ADO provides objects for connecting to data sources, executing commands, retrieving tabular data and schema metadata in a tabular format, and viewing provider error information. ADO MD provides objects for retrieving multidimensional data and viewing multidimensional schema metadata.</span></span>

<span data-ttu-id="57c45-p102">Cuando trabaje con un proveedor de datos multidimensionales (MDP), podrá optar por utilizar ADO, ADO MD, o ambos con su aplicación. Si hace referencia a las dos bibliotecas dentro de su proyecto, tendrá acceso total a la funcionalidad proporcionada por su MDP.</span><span class="sxs-lookup"><span data-stu-id="57c45-p102">When working with an MDP you may choose to use ADO, ADO MD, or both with your application. By referencing both libraries within your project, you will have full access to the functionality provided by your MDP.</span></span>

<span data-ttu-id="57c45-109">Con frecuencia, resulta útil para los usuarios obtener una vista de tabla en dos dimensiones de un conjunto de datos multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="57c45-109">It is often useful for consumers to get a flattened, tabular view of a multidimensional dataset.</span></span> <span data-ttu-id="57c45-110">Para ello, utilice el objeto [Recordset](recordset-object-ado.md) de ADO.</span><span class="sxs-lookup"><span data-stu-id="57c45-110">You can do this by using the ADO [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="57c45-111">Especificar el origen de su [conjunto de celdas](cellset-object-ado-md.md) como el parámetro ***Source*** del método [Open](open-method-ado-recordset.md) de un **conjunto de registros**, en lugar de como el origen para un **conjunto de celdas**de ADO MD.</span><span class="sxs-lookup"><span data-stu-id="57c45-111">Specify the source for your [Cellset](cellset-object-ado-md.md) as the ***Source*** parameter for the [Open](open-method-ado-recordset.md) method of a **Recordset**, rather than as the source for an ADO MD **Cellset**.</span></span>

<span data-ttu-id="57c45-112">También puede resultar útil ver los metadatos de esquema en una vista tabular en lugar de como una jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="57c45-112">It may also be useful to view the schema metadata in a tabular view rather than as a hierarchy of objects.</span></span> <span data-ttu-id="57c45-113">El método [OpenSchema](openschema-method-ado.md) de ADO en el objeto [Connection](connection-object-ado.md) permite al usuario abrir un **conjunto de registros** que contiene información de esquema.</span><span class="sxs-lookup"><span data-stu-id="57c45-113">The ADO [OpenSchema](openschema-method-ado.md) method on the [Connection](connection-object-ado.md) object allows the user to open a **Recordset** containing schema information.</span></span> <span data-ttu-id="57c45-114">El parámetro ***QueryType*** del método **OpenSchema** tiene varios valores [SchemaEnum](schemaenum.md) que se relacionan específicamente con proveedores de datos multidimensionales.</span><span class="sxs-lookup"><span data-stu-id="57c45-114">The ***QueryType*** parameter of the **OpenSchema** method has several [SchemaEnum](schemaenum.md) values that relate specifically to MDPs.</span></span> <span data-ttu-id="57c45-115">Estos valores son:</span><span class="sxs-lookup"><span data-stu-id="57c45-115">These values are:</span></span>

  - <span data-ttu-id="57c45-116">**adSchemaCubes**</span><span class="sxs-lookup"><span data-stu-id="57c45-116">**adSchemaCubes**</span></span>

  - <span data-ttu-id="57c45-117">**adSchemaDimensions**</span><span class="sxs-lookup"><span data-stu-id="57c45-117">**adSchemaDimensions**</span></span>

  - <span data-ttu-id="57c45-118">**adSchemaHierarchies**</span><span class="sxs-lookup"><span data-stu-id="57c45-118">**adSchemaHierarchies**</span></span>

  - <span data-ttu-id="57c45-119">**adSchemaLevels**</span><span class="sxs-lookup"><span data-stu-id="57c45-119">**adSchemaLevels**</span></span>

  - <span data-ttu-id="57c45-120">**adSchemaMeasures**</span><span class="sxs-lookup"><span data-stu-id="57c45-120">**adSchemaMeasures**</span></span>

  - <span data-ttu-id="57c45-121">**adSchemaMembers**</span><span class="sxs-lookup"><span data-stu-id="57c45-121">**adSchemaMembers**</span></span>

<span data-ttu-id="57c45-p105">Para utilizar valores de enumeración de ADO con propiedades o métodos de ADO MD, su proyecto debe hacer referencia a las bibliotecas de ADO y de ADO MD. Por ejemplo, puede utilizar los valores de enumeración **adState** de ADO con la propiedad [State](state-property-ado-md.md) de ADO MD. Para obtener más información acerca del establecimiento de referencias a bibliotecas, vea la documentación de su herramienta de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="57c45-p105">To use ADO enum values with ADO MD properties or methods, your project must reference both the ADO and ADO MD libraries. For example, you can use the ADO **adState** enum values with the ADO MD [State](state-property-ado-md.md) property. For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="57c45-125">Para obtener más información acerca de los objetos y los métodos de ADO, vea la [referencia de API de ADO](ado-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="57c45-125">For more information about the ADO objects and methods, see the [ADO API Reference](ado-api-reference.md).</span></span>

