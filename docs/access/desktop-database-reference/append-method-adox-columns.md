---
title: Append (método, columnas ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861578"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="21255-102">Append (método, columnas ADOX)</span><span class="sxs-lookup"><span data-stu-id="21255-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="21255-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="21255-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="21255-104">Agrega un nuevo objeto [Column](column-object-adox.md) a la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="21255-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="21255-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21255-105">Syntax</span></span>

<span data-ttu-id="21255-106">*Las columnas*.</span><span class="sxs-lookup"><span data-stu-id="21255-106">*Columns*.</span></span> <span data-ttu-id="21255-107">Anexar la*columna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="21255-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="21255-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21255-108">Parameters</span></span>

  - <span data-ttu-id="21255-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="21255-109">*Column*</span></span>

  - <span data-ttu-id="21255-110">El objeto **Column** que se anexará o el nombre de la columna que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="21255-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="21255-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="21255-111">*Type*</span></span>

  - <span data-ttu-id="21255-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="21255-112">Optional.</span></span> <span data-ttu-id="21255-113">Un valor **Long** que especifica el tipo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="21255-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="21255-114">El parámetro *Type* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="21255-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="21255-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="21255-115">*DefinedSize*</span></span>

  - <span data-ttu-id="21255-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="21255-116">Optional.</span></span> <span data-ttu-id="21255-117">Un valor **Long** que especifica el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="21255-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="21255-118">El parámetro *DefinedSize* corresponde a la propiedad [DefinedSize](definedsize-property-adox.md) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="21255-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="21255-119">[!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="21255-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


