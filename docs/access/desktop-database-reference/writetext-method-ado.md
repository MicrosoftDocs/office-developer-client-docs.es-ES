---
title: WriteText (método, ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726249"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="ace2b-102">WriteText (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="ace2b-102">WriteText method (ADO)</span></span>

<span data-ttu-id="ace2b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ace2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ace2b-104">Escribe una cadena de texto especificada en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ace2b-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ace2b-105">Syntax</span></span>

<span data-ttu-id="ace2b-106">*Secuencia*. WriteText*datos*, *Opciones*</span><span class="sxs-lookup"><span data-stu-id="ace2b-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="ace2b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ace2b-107">Parameters</span></span>

|<span data-ttu-id="ace2b-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ace2b-108">Parameter</span></span>|<span data-ttu-id="ace2b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ace2b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ace2b-110">*Datos*</span><span class="sxs-lookup"><span data-stu-id="ace2b-110">*Data*</span></span> |<span data-ttu-id="ace2b-111">Valor de tipo **String** que contiene el texto en caracteres que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="ace2b-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="ace2b-112">*Options*</span><span class="sxs-lookup"><span data-stu-id="ace2b-112">*Options*</span></span> |<span data-ttu-id="ace2b-p101">Es opcional. Valor de [StreamWriteEnum](streamwriteenum.md) que especifica si debe escribirse un carácter separador de línea al final de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="ace2b-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ace2b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ace2b-115">Remarks</span></span>

<span data-ttu-id="ace2b-116">Las cadenas especificadas se escriben en el objeto **Stream** sin espacios ni caracteres intermedios entre ellas.</span><span class="sxs-lookup"><span data-stu-id="ace2b-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="ace2b-p102">El valor de [Position](position-property-ado.md) actual está establecido en el carácter situado después de los datos escritos. El método **WriteText** no trunca el resto de los datos en una secuencia. Si desea truncar estos caracteres, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ace2b-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="ace2b-120">Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) del objeto **Stream** se incrementará para que pueda contener los caracteres nuevos, y \*\* EOS\*\* se moverá hasta el último byte nuevo en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="ace2b-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="ace2b-p103">El método **WriteText** se utiliza para las secuencias de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**). En el caso de las secuencias binarias (el valor de **Type** es **adTypeBinary**), utilice [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ace2b-p103">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>


