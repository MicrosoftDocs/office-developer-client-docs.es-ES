---
title: ReadText (método, ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a44a3a002d390879e5d56d9c6931a91cba40271
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483352"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="c545f-102">ReadText (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="c545f-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="c545f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c545f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c545f-104">Lee un número especificado de caracteres de un objeto [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="c545f-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c545f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c545f-105">Syntax</span></span>

<span data-ttu-id="c545f-106">*Cadena* = *secuencia*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="c545f-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="c545f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c545f-107">Parameters</span></span>

  - <span data-ttu-id="c545f-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="c545f-108">*NumChars*</span></span>

  - <span data-ttu-id="c545f-p101">Es opcional. Valor de tipo **Long** que especifica el número de caracteres que se van a leer en el archivo o un valor de [StreamReadEnum](streamreadenum.md). El valor predeterminado es **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="c545f-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

## <a name="return-value"></a><span data-ttu-id="c545f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c545f-112">Return Value</span></span>

<span data-ttu-id="c545f-113">El método **ReadText** lee un número especificado de caracteres, una línea completa o toda la secuencia de un objeto **Stream** y devuelve la cadena resultante.</span><span class="sxs-lookup"><span data-stu-id="c545f-113">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c545f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c545f-114">Remarks</span></span>

<span data-ttu-id="c545f-p102">Si el valor de *NumChar* es mayor que el número de caracteres que quedan en la secuencia, se devuelven sólo los caracteres restantes. La cadena leída no se rellena para que coincida con la longitud especificada por *NumChar*. Si no quedan caracteres para leer, se devuelve un valor de tipo Variant con el valor null. **ReadText** no se puede utilizar para leer hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="c545f-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c545f-p103">El método <STRONG>ReadText</STRONG> se utiliza para las secuencias de texto (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeText</STRONG>). En el caso de las secuencias binarias (el valor de <STRONG>Type</STRONG> es <STRONG>adTypeBinary</STRONG>), utilice <A href="read-method-ado.md">Read</A>.</span><span class="sxs-lookup"><span data-stu-id="c545f-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


