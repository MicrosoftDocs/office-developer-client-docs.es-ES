---
title: Item (propiedad) (conjunto de celdas de ADO MD)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4f2f67daf4bf072037fac07ecdc3cd163904818
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883802"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="6e3e4-102">Item (propiedad) (conjunto de celdas de ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6e3e4-102">Item Property (ADO MD Cellset)</span></span>

<span data-ttu-id="6e3e4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e3e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e3e4-104">Recupera una celda de un conjunto de celdas utilizando sus coordenadas.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e3e4-105">Syntax</span></span>

<span data-ttu-id="6e3e4-106">Establecer*celda* = *conjunto de celdas*. Elemento (*posiciones*)</span><span class="sxs-lookup"><span data-stu-id="6e3e4-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6e3e4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e3e4-107">Parameters</span></span>

- <span data-ttu-id="6e3e4-108">*Positions*</span><span class="sxs-lookup"><span data-stu-id="6e3e4-108">*Positions*</span></span>

- <span data-ttu-id="6e3e4-109">Una **matriz** **Variant** de valores que especifican inequívocamente una celda.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-109">A **Variant** **Array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="6e3e4-110">*Positions* puede ser una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="6e3e4-110">*Positions* can be one of the following:</span></span>
    
  - <span data-ttu-id="6e3e4-111">Una matriz de números de posiciones</span><span class="sxs-lookup"><span data-stu-id="6e3e4-111">An array of position numbers</span></span>
    
  - <span data-ttu-id="6e3e4-112">Una matriz de nombres de miembros</span><span class="sxs-lookup"><span data-stu-id="6e3e4-112">An array of member names</span></span>
    
  - <span data-ttu-id="6e3e4-113">La posición ordinal</span><span class="sxs-lookup"><span data-stu-id="6e3e4-113">The ordinal position</span></span>

## <a name="remarks"></a><span data-ttu-id="6e3e4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e3e4-114">Remarks</span></span>

<span data-ttu-id="6e3e4-115">Utilice la propiedad **Item** para devolver un objeto [Cell](cell-object-ado-md.md) dentro de un objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="6e3e4-115">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="6e3e4-116">Si la propiedad **Item** no puede encontrar la celda correspondiente al argumento *Positions* , se produce un error.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-116">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="6e3e4-p103">**Item** es la propiedad predeterminada para el objeto **Cellset**. Los siguientes formatos de sintaxis son intercambiables:</span><span class="sxs-lookup"><span data-stu-id="6e3e4-p103">The **Item** property is the default property for the **Cellset** object. The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="6e3e4-119">El argumento *Positions* especifica la celda que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-119">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="6e3e4-120">Puede especificar la celda por la posición ordinal o por la posición a lo largo del eje.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-120">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="6e3e4-121">Cuando se especifica por la posición a lo largo del eje, puede indicar el valor numérico de la posición o los nombres de los miembros de cada posición.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-121">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="6e3e4-p105">La posición ordinal es un número que identifica inequívocamente una celda dentro del **conjunto de celdas**. Conceptualmente, las celdas se numeran en un **conjunto de celdas** como si el **conjunto de celdas** fuera una matriz de *p* dimensiones, donde *p* es el número de ejes. El tratamiento de las celdas sigue el orden de fila mayor.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-p105">The ordinal position is a number that uniquely identifies one cell within the **Cellset**. Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes. Cells are addressed in row-major order.</span></span>

<span data-ttu-id="6e3e4-p106">Si se pasan nombres de miembros como cadenas al objeto **Item**, los miembros deben especificarse siguiendo el orden creciente de los identificadores de eje numérico. Dentro de un eje, los miembros deben especificarse en orden creciente de las dimensiones anidadas , es decir, primero el miembro de la dimensión exterior y después los miembros de las dimensiones interiores. Cada dimensión debe representarse mediante una cadena distinta, y la lista de cadenas de miembro debe separarse por comas.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-p106">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers. Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions. Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="6e3e4-p107">[!NOTA] Puede que el proveedor de datos no permita la recuperación de celdas por nombre de miembro. Vea la documentación de su proveedor para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6e3e4-p107">Retrieving cells by member name may not be supported by your data provider. See the documentation for your provider for more information.</span></span>


