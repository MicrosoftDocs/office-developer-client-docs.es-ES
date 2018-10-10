---
title: Append (método, claves ADOX)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486222"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="e7336-102">Append (método, claves ADOX)</span><span class="sxs-lookup"><span data-stu-id="e7336-102">Append Method (ADOX Keys)</span></span>


<span data-ttu-id="e7336-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7336-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="e7336-104">Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e7336-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7336-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7336-105">Syntax</span></span>

<span data-ttu-id="e7336-106">*Las claves*. Anexar*clave* \[,*tipo de clave* \] \[,*columna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="e7336-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="e7336-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7336-107">Parameters</span></span>

  - <span data-ttu-id="e7336-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="e7336-108">*Key*</span></span>

  - <span data-ttu-id="e7336-109">El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="e7336-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="e7336-110">*Tipo de clave*</span><span class="sxs-lookup"><span data-stu-id="e7336-110">*KeyType*</span></span>

  - <span data-ttu-id="e7336-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7336-111">Optional.</span></span> <span data-ttu-id="e7336-112">Un valor **Long** que especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="e7336-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="e7336-113">El parámetro *clave* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) de un objeto **Key** .</span><span class="sxs-lookup"><span data-stu-id="e7336-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="e7336-114">*Column*</span><span class="sxs-lookup"><span data-stu-id="e7336-114">*Column*</span></span>

  - <span data-ttu-id="e7336-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7336-115">Optional.</span></span> <span data-ttu-id="e7336-116">Un valor **String** que especifica el nombre de la columna que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="e7336-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="e7336-117">El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e7336-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="e7336-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="e7336-118">*RelatedTable*</span></span>

  - <span data-ttu-id="e7336-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e7336-119">Optional.</span></span> <span data-ttu-id="e7336-120">Un valor **String** que especifica el nombre de la tabla relacionada.</span><span class="sxs-lookup"><span data-stu-id="e7336-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="e7336-121">El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e7336-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="e7336-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="e7336-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="e7336-p104">Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="e7336-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7336-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7336-126">Remarks</span></span>

<span data-ttu-id="e7336-127">El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="e7336-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

