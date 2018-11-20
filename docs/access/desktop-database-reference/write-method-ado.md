---
title: Escribir el método - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 227c7a3746d0c743c33f76362023d6d374269a81
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026284"
---
# <a name="write-method-ado"></a><span data-ttu-id="1700d-102">Write (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="1700d-102">Write method (ADO)</span></span>

<span data-ttu-id="1700d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1700d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1700d-104">Escribe datos binarios en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1700d-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1700d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1700d-105">Syntax</span></span>

<span data-ttu-id="1700d-106">*Secuencia*. *Búfer* de escritura</span><span class="sxs-lookup"><span data-stu-id="1700d-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="1700d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1700d-107">Parameters</span></span>

|<span data-ttu-id="1700d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1700d-108">Parameter</span></span>|<span data-ttu-id="1700d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1700d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1700d-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="1700d-110">*Buffer*</span></span> |<span data-ttu-id="1700d-111">**Variant** que contiene la matriz de bytes que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="1700d-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1700d-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1700d-112">Remarks</span></span>

<span data-ttu-id="1700d-113">Los bytes especificados se escriben en el objeto **Stream** sin espacios intermedios entre ellos.</span><span class="sxs-lookup"><span data-stu-id="1700d-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="1700d-p101">El valor de [Position](position-property-ado.md) actual está establecido en el byte situado después de los datos escritos. El método **Write** no trunca el resto de los datos en una secuencia. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1700d-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="1700d-117">Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) del objeto **Stream** se incrementará para que pueda contener los bytes nuevos, y \*\* EOS\*\* se moverá hasta el último byte nuevo en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="1700d-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="1700d-p102">El método **Write** se utiliza con secuencias binarias (el valor de [Type](type-property-ado-stream.md) es **adTypeBinary**). Utilice [WriteText](writetext-method-ado.md) para las secuencias de texto (el valor de **Type** es **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="1700d-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

