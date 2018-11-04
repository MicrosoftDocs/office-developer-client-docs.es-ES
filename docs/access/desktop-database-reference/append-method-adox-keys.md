---
title: Append (método, Keys de ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d99af00f1ad83087994737f5bb3ca29acf2a9deb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949820"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="ce345-102">Append (método, Keys de ADOX)</span><span class="sxs-lookup"><span data-stu-id="ce345-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="ce345-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce345-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce345-104">Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ce345-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce345-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce345-105">Syntax</span></span>

<span data-ttu-id="ce345-106">*Las claves*. Anexar*clave* \[,*tipo de clave* \] \[,*columna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="ce345-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="ce345-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce345-107">Parameters</span></span>

|<span data-ttu-id="ce345-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ce345-108">Parameter</span></span>|<span data-ttu-id="ce345-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce345-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ce345-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="ce345-110">*Key*</span></span> |<span data-ttu-id="ce345-111">El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="ce345-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="ce345-112">*Tipo de clave*</span><span class="sxs-lookup"><span data-stu-id="ce345-112">*KeyType*</span></span> |<span data-ttu-id="ce345-113">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ce345-113">Optional.</span></span> <span data-ttu-id="ce345-114">Un valor **Long** que especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="ce345-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="ce345-115">El parámetro *clave* corresponde a la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de un objeto **Key** .</span><span class="sxs-lookup"><span data-stu-id="ce345-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="ce345-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="ce345-116">*Column*</span></span> |<span data-ttu-id="ce345-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ce345-117">Optional.</span></span> <span data-ttu-id="ce345-118">Un valor **String** que especifica el nombre de la columna que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="ce345-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="ce345-119">El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ce345-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="ce345-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="ce345-120">*RelatedTable*</span></span> |<span data-ttu-id="ce345-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ce345-121">Optional.</span></span> <span data-ttu-id="ce345-122">Un valor **String** que especifica el nombre de la tabla relacionada.</span><span class="sxs-lookup"><span data-stu-id="ce345-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="ce345-123">El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ce345-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="ce345-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="ce345-124">*RelatedColumn*</span></span> |<span data-ttu-id="ce345-p104">Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="ce345-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ce345-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce345-128">Remarks</span></span>

<span data-ttu-id="ce345-129">El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="ce345-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

