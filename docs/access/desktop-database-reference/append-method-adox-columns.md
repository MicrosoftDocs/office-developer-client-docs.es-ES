---
title: Append (método, columnas ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483797"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="06eb8-102">Append (método, columnas ADOX)</span><span class="sxs-lookup"><span data-stu-id="06eb8-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="06eb8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="06eb8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="06eb8-104">Agrega un nuevo objeto [Column](column-object-adox.md) a la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="06eb8-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="06eb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06eb8-105">Syntax</span></span>

<span data-ttu-id="06eb8-106">*Las columnas*.</span><span class="sxs-lookup"><span data-stu-id="06eb8-106">*Columns*.</span></span> <span data-ttu-id="06eb8-107">Anexar la*columna* \[,*tipo* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="06eb8-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="06eb8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06eb8-108">Parameters</span></span>

  - <span data-ttu-id="06eb8-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="06eb8-109">*Column*</span></span>

  - <span data-ttu-id="06eb8-110">El objeto **Column** que se anexará o el nombre de la columna que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="06eb8-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="06eb8-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="06eb8-111">*Type*</span></span>

  - <span data-ttu-id="06eb8-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="06eb8-112">Optional.</span></span> <span data-ttu-id="06eb8-113">Un valor **Long** que especifica el tipo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="06eb8-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="06eb8-114">El parámetro *Type* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="06eb8-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="06eb8-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="06eb8-115">*DefinedSize*</span></span>

  - <span data-ttu-id="06eb8-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="06eb8-116">Optional.</span></span> <span data-ttu-id="06eb8-117">Un valor **Long** que especifica el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="06eb8-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="06eb8-118">El parámetro *DefinedSize* corresponde a la propiedad [DefinedSize](definedsize-property-adox.md) de un objeto **Column** .</span><span class="sxs-lookup"><span data-stu-id="06eb8-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="06eb8-119">[!NOTA] Si se anexa una <STRONG>columna</STRONG> a la colección <STRONG>Columns</STRONG> de un <A href="index-object-adox.md">índice</A> pero la <STRONG>columna</STRONG> no existe en alguna <A href="table-object-adox.md">tabla</A> que ya se haya anexado a la colección <A href="tables-collection-adox.md">Tables</A>, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="06eb8-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


