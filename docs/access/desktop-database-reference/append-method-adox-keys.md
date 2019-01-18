---
title: Append (método, Keys de ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718906"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="81c1c-102">Append (método, Keys de ADOX)</span><span class="sxs-lookup"><span data-stu-id="81c1c-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="81c1c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81c1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81c1c-104">Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="81c1c-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81c1c-105">Syntax</span></span>

<span data-ttu-id="81c1c-106">*Las claves*. Anexar*clave* \[,*tipo de clave* \] \[,*columna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="81c1c-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="81c1c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81c1c-107">Parameters</span></span>

|<span data-ttu-id="81c1c-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="81c1c-108">Parameter</span></span>|<span data-ttu-id="81c1c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="81c1c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81c1c-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="81c1c-110">*Key*</span></span> |<span data-ttu-id="81c1c-111">El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="81c1c-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="81c1c-112">*Tipo de clave*</span><span class="sxs-lookup"><span data-stu-id="81c1c-112">*KeyType*</span></span> |<span data-ttu-id="81c1c-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="81c1c-113">Optional.</span></span> <span data-ttu-id="81c1c-114">Un valor **Long** que especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="81c1c-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="81c1c-115">El parámetro *clave* corresponde a la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de un objeto **Key** .</span><span class="sxs-lookup"><span data-stu-id="81c1c-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="81c1c-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="81c1c-116">*Column*</span></span> |<span data-ttu-id="81c1c-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="81c1c-117">Optional.</span></span> <span data-ttu-id="81c1c-118">Un valor **String** que especifica el nombre de la columna que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="81c1c-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="81c1c-119">El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="81c1c-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="81c1c-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="81c1c-120">*RelatedTable*</span></span> |<span data-ttu-id="81c1c-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="81c1c-121">Optional.</span></span> <span data-ttu-id="81c1c-122">Un valor **String** que especifica el nombre de la tabla relacionada.</span><span class="sxs-lookup"><span data-stu-id="81c1c-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="81c1c-123">El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="81c1c-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="81c1c-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="81c1c-124">*RelatedColumn*</span></span> |<span data-ttu-id="81c1c-p104">Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="81c1c-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81c1c-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81c1c-128">Remarks</span></span>

<span data-ttu-id="81c1c-129">El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="81c1c-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

