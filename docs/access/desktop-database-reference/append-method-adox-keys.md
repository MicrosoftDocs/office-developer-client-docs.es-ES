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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297091"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="b21a5-102">Append (método, Keys de ADOX)</span><span class="sxs-lookup"><span data-stu-id="b21a5-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="b21a5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b21a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b21a5-104">Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b21a5-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b21a5-105">Syntax</span></span>

<span data-ttu-id="b21a5-106">*Claves*. Append *Key* \[ ,*KeyType* \] \[ ,*Column* \] \[ ,*RelatedTable* \] \[ ,*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="b21a5-106">*Keys*.Append *Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b21a5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b21a5-107">Parameters</span></span>

|<span data-ttu-id="b21a5-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b21a5-108">Parameter</span></span>|<span data-ttu-id="b21a5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b21a5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b21a5-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="b21a5-110">*Key*</span></span> |<span data-ttu-id="b21a5-111">El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.</span><span class="sxs-lookup"><span data-stu-id="b21a5-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="b21a5-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="b21a5-112">*KeyType*</span></span> |<span data-ttu-id="b21a5-p101">Opcional. Un valor **Long** que especifica el tipo de clave. El parámetro *KeyType* corresponde a la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de un objeto **Key**.</span><span class="sxs-lookup"><span data-stu-id="b21a5-p101">Optional. A **Long** value that specifies the type of key. The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="b21a5-116">*Columna*</span><span class="sxs-lookup"><span data-stu-id="b21a5-116">*Column*</span></span> |<span data-ttu-id="b21a5-p102">Opcional. Un valor **String** que especifica el nombre de la columna que se va a indizar. El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b21a5-p102">Optional. A **String** value that specifies the name of the column to be indexed. The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="b21a5-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="b21a5-120">*RelatedTable*</span></span> |<span data-ttu-id="b21a5-p103">Opcional. Un valor **String** que especifica el nombre de la tabla relacionada. El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b21a5-p103">Optional. A **String** value that specifies the name of the related table. The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="b21a5-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="b21a5-124">*RelatedColumn*</span></span> |<span data-ttu-id="b21a5-p104">Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.</span><span class="sxs-lookup"><span data-stu-id="b21a5-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b21a5-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b21a5-128">Remarks</span></span>

<span data-ttu-id="b21a5-129">El parámetro *Columns* puede tomar el nombre de una columna, o bien, de una matriz de nombres de columna.</span><span class="sxs-lookup"><span data-stu-id="b21a5-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

