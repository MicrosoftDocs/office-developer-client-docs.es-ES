---
title: Lea el método - ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cdbf9bc7ab29b98c7d1b96700adccaa17275d698
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946555"
---
# <a name="read-method-ado"></a><span data-ttu-id="c8ef1-102">Read (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="c8ef1-102">Read method (ADO)</span></span>


<span data-ttu-id="c8ef1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8ef1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8ef1-104">Lee un número especificado de bytes de un objeto [Stream](stream-object-ado.md) binario.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ef1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8ef1-105">Syntax</span></span>

<span data-ttu-id="c8ef1-106">*Variant* = *secuencia*. Lectura (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="c8ef1-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="c8ef1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8ef1-107">Parameters</span></span>

  - <span data-ttu-id="c8ef1-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="c8ef1-108">*NumBytes*</span></span>

  - <span data-ttu-id="c8ef1-p101">Es opcional. Valor de tipo **Long** que especifica el número de bytes que se van a leer en el archivo, o bien, el valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8ef1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8ef1-111">Return value</span></span>

<span data-ttu-id="c8ef1-112">El método **Read** lee un número especificado de bytes o toda la secuencia de un objeto **Stream** y devuelve los datos resultantes como un valor de tipo **Variant**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8ef1-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8ef1-113">Remarks</span></span>

<span data-ttu-id="c8ef1-p102">Si el valor de *NumBytes* es mayor que el número de bytes que quedan en el objeto **Stream**, se devolverán sólo los bytes restantes. Los datos leídos no se rellenan para que coincidan con la longitud especificada por *NumBytes*. Si ya no quedan bytes para leer, se devuelve un valor de tipo Variant con el valor null. El método **Read** no se puede utilizar para leer hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c8ef1-p103"><EM>NumBytes</EM> siempre mide los bytes. En el caso de los objetos <STRONG>Stream</STRONG> de texto (el valor de <A href="type-property-ado-stream.md">Type</A> es <STRONG>adTypeText</STRONG>), utilice <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


