---
title: WriteText (método, ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b457af35e0b9b5f7d61bf5a77f080a11b36232ae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884096"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="c47b6-102">WriteText (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="c47b6-102">WriteText Method (ADO)</span></span>


<span data-ttu-id="c47b6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c47b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c47b6-104">Escribe una cadena de texto especificada en un objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c47b6-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c47b6-105">Syntax</span></span>

<span data-ttu-id="c47b6-106">*Secuencia*. WriteText*datos*, *Opciones*</span><span class="sxs-lookup"><span data-stu-id="c47b6-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="c47b6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c47b6-107">Parameters</span></span>

  - <span data-ttu-id="c47b6-108">*Data*</span><span class="sxs-lookup"><span data-stu-id="c47b6-108">*Data*</span></span>

  - <span data-ttu-id="c47b6-109">Valor de tipo **String** que contiene el texto en caracteres que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="c47b6-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="c47b6-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="c47b6-110">*Options*</span></span>

  - <span data-ttu-id="c47b6-p101">Es opcional. Valor de [StreamWriteEnum](streamwriteenum.md) que especifica si debe escribirse un carácter separador de línea al final de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="c47b6-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c47b6-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c47b6-113">Remarks</span></span>

<span data-ttu-id="c47b6-114">Las cadenas especificadas se escriben en el objeto **Stream** sin espacios ni caracteres intermedios entre ellas.</span><span class="sxs-lookup"><span data-stu-id="c47b6-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="c47b6-p102">El valor de [Position](position-property-ado.md) actual está establecido en el carácter situado después de los datos escritos. El método **WriteText** no trunca el resto de los datos en una secuencia. Si desea truncar estos caracteres, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c47b6-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="c47b6-118">Si escribe más allá de la actual posición de [EOS](eos-property-ado.md), el valor de [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) del objeto **Stream** se incrementará para que pueda contener los caracteres nuevos, y \*\* EOS\*\* se moverá hasta el último byte nuevo en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="c47b6-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c47b6-p103">El método <STRONG>WriteText</STRONG> se utiliza para las secuencias de texto (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeText</STRONG>). En el caso de las secuencias binarias (el valor de <STRONG>Type</STRONG> es <STRONG>adTypeBinary</STRONG>), utilice <A href="write-method-ado.md">Write</A>.</span><span class="sxs-lookup"><span data-stu-id="c47b6-p103">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>


