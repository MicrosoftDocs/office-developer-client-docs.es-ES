---
title: CreateParameter (método, ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d3b36d04345df4c1d556d0607c70b3425f0047e6
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949961"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="69a7c-102">CreateParameter (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="69a7c-102">CreateParameter method (ADO)</span></span>

<span data-ttu-id="69a7c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69a7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69a7c-104">Crea un nuevo objeto [Parameter](parameter-object-ado.md) con las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="69a7c-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69a7c-105">Syntax</span></span>

<span data-ttu-id="69a7c-106">**Establecer** *parámetro*  =  *comando*. CreateParameter (*nombre*, *tipo*, *dirección*, *tamaño*, *valor*)</span><span class="sxs-lookup"><span data-stu-id="69a7c-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="69a7c-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69a7c-107">Return value</span></span>

<span data-ttu-id="69a7c-108">Devuelve un objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="69a7c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69a7c-109">Parameters</span></span>

|<span data-ttu-id="69a7c-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="69a7c-110">Parameter</span></span>|<span data-ttu-id="69a7c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="69a7c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69a7c-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="69a7c-112">*Name*</span></span> |<span data-ttu-id="69a7c-p101">Es opcional. Valor de tipo **String** que contiene el nombre del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>|
|<span data-ttu-id="69a7c-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="69a7c-115">*Type*</span></span> |<span data-ttu-id="69a7c-p102">Es opcional. Valor de [DataTypeEnum](datatypeenum.md) que especifica el tipo de datos del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>|
|<span data-ttu-id="69a7c-118">*Direction*</span><span class="sxs-lookup"><span data-stu-id="69a7c-118">*Direction*</span></span> |<span data-ttu-id="69a7c-p103">Es opcional. Valor de [ParameterDirectionEnum](parameterdirectionenum.md) que especifica el tipo del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>|
|<span data-ttu-id="69a7c-121">*Size*</span><span class="sxs-lookup"><span data-stu-id="69a7c-121">*Size*</span></span> |<span data-ttu-id="69a7c-p104">Es opcional. Valor de tipo **Long** que especifica la longitud máxima del valor de parámetro, en caracteres o bytes.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>|
|<span data-ttu-id="69a7c-124">*Valor*</span><span class="sxs-lookup"><span data-stu-id="69a7c-124">*Value*</span></span> |<span data-ttu-id="69a7c-p105">Es opcional. **Variant** que especifica el valor del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="69a7c-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69a7c-127">Remarks</span></span>

<span data-ttu-id="69a7c-p106">Utilice el método **CreateParameter** para crear un nuevo objeto **Parameter** con un nombre, un tipo, una dirección, un tamaño y un valor especificados. Cualquier valor que pase en los argumentos se escribe en las correspondientes propiedades de **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="69a7c-p107">Este método no anexa automáticamente el objeto **Parameter** a la colección **Parameters** de un objeto [Command](command-object-ado.md). Esto le permite establecer propiedades adicionales cuyos valores ADO validará cuando se anexe el objeto **Parameter** a la colección.</span><span class="sxs-lookup"><span data-stu-id="69a7c-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="69a7c-132">Si especifica un tipo de datos de longitud variable en el argumento *Type* , debe pasar un argumento *Size* o establecer la propiedad [Size](size-property-ado.md) del objeto **Parameter** antes de agregarlo a la colección de **parámetros** . de lo contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="69a7c-132">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="69a7c-133">Si especifica un tipo de datos numérico (**adNumeric** o **adDecimal**) en el argumento *Type*, también deberá establecer las propiedades [NumericScale](numericscale-property-ado.md) y [Precision](precision-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="69a7c-133">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

