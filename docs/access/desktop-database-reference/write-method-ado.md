---
title: Escribir el método - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867415"
---
# <a name="write-method-ado"></a><span data-ttu-id="29db8-102">Write (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="29db8-102">Write Method (ADO)</span></span>


<span data-ttu-id="29db8-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29db8-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="29db8-104">Escribe datos binarios en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="29db8-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="29db8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29db8-105">Syntax</span></span>

<span data-ttu-id="29db8-106">*Secuencia*. *Búfer* de escritura</span><span class="sxs-lookup"><span data-stu-id="29db8-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="29db8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29db8-107">Parameters</span></span>

  - <span data-ttu-id="29db8-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="29db8-108">*Buffer*</span></span>

  - <span data-ttu-id="29db8-109">**Variant** que contiene la matriz de bytes que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="29db8-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="29db8-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29db8-110">Remarks</span></span>

<span data-ttu-id="29db8-111">Los bytes especificados se escriben en el objeto **Stream** sin espacios intermedios entre ellos.</span><span class="sxs-lookup"><span data-stu-id="29db8-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="29db8-p101">El valor de [Position](position-property-ado.md) actual está establecido en el byte situado después de los datos escritos. El método **Write** no trunca el resto de los datos en una secuencia. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="29db8-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="29db8-115">Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** se incrementará para que pueda contener los bytes nuevos, y \*\* EOS\*\* se moverá hasta el último byte nuevo en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="29db8-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="29db8-p102">El método <STRONG>Write</STRONG> se utiliza con secuencias binarias (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeBinary</STRONG>). Utilice <A href="writetext-method-ado.md">WriteText</A> para las secuencias de texto (el valor de <STRONG>Type</STRONG> es <STRONG>adTypeText</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="29db8-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


