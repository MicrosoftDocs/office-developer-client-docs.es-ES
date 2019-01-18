---
title: ReadText (método, ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699936"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="1b6d2-102">ReadText (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="1b6d2-102">ReadText method (ADO)</span></span>

<span data-ttu-id="1b6d2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b6d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b6d2-104">Lee un número especificado de caracteres de un objeto [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="1b6d2-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b6d2-105">Syntax</span></span>

<span data-ttu-id="1b6d2-106">*Cadena* = *secuencia*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="1b6d2-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1b6d2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b6d2-107">Parameters</span></span>

|<span data-ttu-id="1b6d2-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1b6d2-108">Parameter</span></span>|<span data-ttu-id="1b6d2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b6d2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1b6d2-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="1b6d2-110">*NumChars*</span></span> |<span data-ttu-id="1b6d2-p101">Es opcional. Valor de tipo **Long** que especifica el número de caracteres que se van a leer en el archivo o un valor de [StreamReadEnum](streamreadenum.md). El valor predeterminado es **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="1b6d2-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="1b6d2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b6d2-114">Return value</span></span>

<span data-ttu-id="1b6d2-115">El método **ReadText** lee un número especificado de caracteres, una línea completa o toda la secuencia de un objeto **Stream** y devuelve la cadena resultante.</span><span class="sxs-lookup"><span data-stu-id="1b6d2-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b6d2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b6d2-116">Remarks</span></span>

<span data-ttu-id="1b6d2-p102">Si el valor de *NumChar* es mayor que el número de caracteres que quedan en la secuencia, se devuelven sólo los caracteres restantes. La cadena leída no se rellena para que coincida con la longitud especificada por *NumChar*. Si no quedan caracteres para leer, se devuelve un valor de tipo Variant con el valor null. **ReadText** no se puede utilizar para leer hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="1b6d2-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="1b6d2-p103">El método **ReadText** se utiliza para las secuencias de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**). En el caso de las secuencias binarias (el valor de **Type** es **adTypeBinary**), utilice [Read](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1b6d2-p103">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>

