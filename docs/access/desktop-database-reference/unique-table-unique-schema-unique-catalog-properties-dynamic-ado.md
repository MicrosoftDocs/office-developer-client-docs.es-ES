---
title: Unique Table, Unique Schema, las propiedades dinámicas Unique Catalog (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b2c3c87a820638b74e74c513443261e052e2c4d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919433"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="be3a3-102">Unique Table, Unique Schema, las propiedades dinámicas Unique Catalog (ADO)</span><span class="sxs-lookup"><span data-stu-id="be3a3-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="be3a3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be3a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be3a3-104">Permiten controlar estrechamente las modificaciones realizadas en una tabla base concreta de un objeto [Recordset](recordset-object-ado.md) formado mediante una operación JOIN en varias tablas base.</span><span class="sxs-lookup"><span data-stu-id="be3a3-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="be3a3-105">**Unique Table** especifica el nombre de la tabla base en la que se permiten actualizaciones, inserciones y eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="be3a3-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="be3a3-106">**Unique Schema** especifica el *esquema* o el nombre del propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="be3a3-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="be3a3-107">**Unique Catalog** especifica el *catálogo* o el nombre de la base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="be3a3-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="be3a3-108">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="be3a3-108">Settings and return values</span></span>

<span data-ttu-id="be3a3-109">Establecen o devuelven un valor de tipo **String** que es el nombre de una tabla, un esquema o un catálogo.</span><span class="sxs-lookup"><span data-stu-id="be3a3-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3a3-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be3a3-110">Remarks</span></span>

<span data-ttu-id="be3a3-p101">La tabla base deseada es identificada de forma exclusiva por el nombre de catálogo, esquema y tabla. Cuando se establece la propiedad **Unique Table**, los valores de las propiedades **Unique Schema** o **Unique Catalog** se utilizan para buscar la tabla base. Se recomienda, aunque no es obligatorio, que alguna de las propiedades **Unique Schema** y **Unique Catalog** o ambas se establezcan antes de establecer la propiedad **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="be3a3-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="be3a3-p102">La clave principal de **Unique Table** se trata como la clave principal de todo el objeto **Recordset**. Esta es la clave que se usa con cualquier método que exija una clave principal.</span><span class="sxs-lookup"><span data-stu-id="be3a3-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="be3a3-p103">Mientras se establece **Unique Table**, el método [Delete](delete-method-ado-recordset.md) sólo afecta a la tabla con nombre. Los métodos [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) y [UpdateBatch](updatebatch-method-ado.md) afectan a cualquier tabla base subyacente de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="be3a3-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="be3a3-p104">**Unique Table** debe especificarse antes de volver a realizar cualquier sincronización personalizada. Si **Unique Table** no se ha especificado, la propiedad [Resync Command](resync-command-property-dynamic-ado.md) no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="be3a3-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="be3a3-120">Si no se puede encontrar una tabla base exclusiva, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="be3a3-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="be3a3-121">Todas estas propiedades dinámicas se anexan a la colección **Properties** del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="be3a3-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

