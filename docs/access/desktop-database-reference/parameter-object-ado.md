---
title: Parameter (objeto) (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d6f3acd4af280f30706e35eb7ecda1dee11aa7d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288080"
---
# <a name="parameter-object-ado"></a><span data-ttu-id="d69fb-102">Parameter (objeto) (ADO)</span><span class="sxs-lookup"><span data-stu-id="d69fb-102">Parameter object (ADO)</span></span>


<span data-ttu-id="d69fb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d69fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d69fb-104">Representa un parámetro o un argumento asociado a un objeto [Command](command-object-ado.md) basado en una consulta parametrizada o un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="d69fb-104">Represents a parameter or argument associated with a [Command](command-object-ado.md) object based on a parameterized query or stored procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d69fb-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d69fb-105">Remarks</span></span>

<span data-ttu-id="d69fb-p101">Gran número de proveedores admiten comandos parametrizados. Se trata de comandos en los que la acción deseada se define una vez, pero se usan variables (o parámetros) para modificar algunos detalles del comando. Por ejemplo, una instrucción SELECT de SQL podría usar un parámetro para definir los criterios de coincidencia de una cláusula WHERE y otro parámetro para definir el nombre de columna para una cláusula SORT BY.</span><span class="sxs-lookup"><span data-stu-id="d69fb-p101">Many providers support parameterized commands. These are commands in which the desired action is defined once, but variables (or parameters) are used to alter some details of the command. For example, an SQL SELECT statement could use a parameter to define the matching criteria of a WHERE clause, and another to define the column name for a SORT BY clause.</span></span>

<span data-ttu-id="d69fb-p102">Los objetos **Parameter** representan parámetros asociados a consultas parametrizadas, o los argumentos de entrada/salida y los valores devueltos de procedimientos almacenados. Dependiendo de la funcionalidad del proveedor, es posible que algunas colecciones, métodos o propiedades de un objeto **Parameter** no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="d69fb-p102">**Parameter** objects represent parameters associated with parameterized queries, or the in/out arguments and the return values of stored procedures. Depending on the functionality of the provider, some collections, methods, or properties of a **Parameter** object may not be available.</span></span>

<span data-ttu-id="d69fb-111">Con las colecciones, los métodos y las propiedades de un objeto **Parameter**, se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d69fb-111">With the collections, methods, and properties of a **Parameter** object, you can do the following:</span></span>

  - <span data-ttu-id="d69fb-112">Establecer o devolver el nombre de un parámetro con la propiedad [Name](name-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d69fb-112">Set or return the name of a parameter with the [Name](name-property-ado.md) property.</span></span>

  - <span data-ttu-id="d69fb-p103">Establecer o devolver el valor de un parámetro con la propiedad [Value](value-property-ado.md). **Value** es la propiedad predeterminada del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d69fb-p103">Set or return the value of a parameter with the [Value](value-property-ado.md) property. **Value** is the default property of the **Parameter** object.</span></span>

  - <span data-ttu-id="d69fb-115">Establecer o devolver las características de los parámetros con las propiedades [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) y [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d69fb-115">Set or return parameter characteristics with the [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md), and [Type](type-property-ado.md) properties.</span></span>

  - <span data-ttu-id="d69fb-116">Pasar datos de caracteres largos o binarios largos a un parámetro con el método [AppendChunk](appendchunk-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d69fb-116">Pass long binary or character data to a parameter with the [AppendChunk](appendchunk-method-ado.md) method.</span></span>

  - <span data-ttu-id="d69fb-117">Obtener acceso a atributos específicos del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d69fb-117">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="d69fb-p104">Si sabe los nombres y las propiedades de los parámetros asociados al procedimiento almacenado o a la consulta parametrizada que desea invocar, puede usar el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados, y utilizar el método [Append](append-method-ado.md) para agregarlos a la colección [Parameters](parameters-collection-ado.md). Esto permite establecer y devolver valores de parámetro sin tener que llamar al método [Refresh](refresh-method-ado.md) en la colección **Parameters** para recuperar la información sobre parámetros del proveedor, una operación que puede utilizar muchos recursos.</span><span class="sxs-lookup"><span data-stu-id="d69fb-p104">If you know the names and properties of the parameters associated with the stored procedure or parameterized query you wish to call, you can use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the [Refresh](refresh-method-ado.md) method on the **Parameters** collection to retrieve the parameter information from the provider, a potentially resource-intensive operation.</span></span>

