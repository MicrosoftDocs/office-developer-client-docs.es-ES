---
title: Método CopyTo (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295481"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="c9a1d-102">Método CopyTo (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9a1d-102">CopyTo method (ADO)</span></span>

<span data-ttu-id="c9a1d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9a1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9a1d-104">Copia el número especificado de caracteres o bytes (según [Type](type-property-ado-stream.md)) de un objeto [Stream](stream-object-ado.md) a otro objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9a1d-105">Syntax</span></span>

<span data-ttu-id="c9a1d-106">*Stream*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="c9a1d-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="c9a1d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9a1d-107">Parameters</span></span>

|<span data-ttu-id="c9a1d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c9a1d-108">Parameter</span></span>|<span data-ttu-id="c9a1d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9a1d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9a1d-110">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="c9a1d-110">*DestStream*</span></span> |<span data-ttu-id="c9a1d-111">Valor de variable de objeto que contiene una referencia a un objeto **Stream** abierto.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-111">An object variable value that contains a reference to an open **Stream** object.</span></span> <span data-ttu-id="c9a1d-112">El actual objeto **Stream** se copia en el objeto **Stream** de destino especificado por *DestStream*.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-112">The current **Stream** is copied to the destination **Stream** specified by *DestStream*.</span></span> <span data-ttu-id="c9a1d-113">El objeto **Stream** de destino ya debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-113">The destination **Stream** must already be open.</span></span> <span data-ttu-id="c9a1d-114">De lo contrario, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-114">If not, a run-time error occurs.</span></span><br/><br/><span data-ttu-id="c9a1d-115">**NOTA:** Es posible que el parámetro *DestStream* no sea un proxy del objeto **Stream** porque esto requiere acceso a una interfaz privada en el objeto **Stream** que no se puede remotar para el cliente.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-115">**NOTE**: The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>|
|<span data-ttu-id="c9a1d-116">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="c9a1d-116">*NumChars*</span></span> |<span data-ttu-id="c9a1d-p102">Es opcional. Valor de tipo **Integer** que especifica el número de bytes o caracteres que se van a copiar a partir de la actual posición en el objeto **Stream** de origen al objeto **Stream** de destino. El valor predeterminado es –1, que especifica que se van a copiar todos los caracteres o bytes desde la posición actual hasta [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c9a1d-p102">Optional. An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**. The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>|

## <a name="remarks"></a><span data-ttu-id="c9a1d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9a1d-120">Remarks</span></span>

<span data-ttu-id="c9a1d-p103">Este método copia el número especificado de caracteres o bytes, a partir de la actual posición especificada por la propiedad [Position](position-property-ado.md). Si el número especificado es mayor que el número de bytes disponibles hasta **EOS**, sólo se copiarán los caracteres o bytes desde la posición actual hasta **EOS**. Si el valor de *NumChars* es –1 o se omite, se copiarán todos los caracteres o bytes a partir de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-p103">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property. If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied. If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="c9a1d-p104">Si hay caracteres o bytes en la secuencia de destino, se mantiene todo el contenido situado más allá del punto donde finaliza la copia y no se ve truncado. El valor de **Position** será el byte inmediatamente después del último byte copiado. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c9a1d-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="c9a1d-p105">**CopyTo** debe utilizarse para copiar datos a un objeto **Stream** de destino del mismo tipo que el objeto **Stream** de origen (el valor de la propiedad **Type** de ambos objetos debe ser **adTypeText** o **adTypeBinary**). Para los objetos **Stream** de texto, puede cambiar la configuración de la propiedad [Charset](charset-property-ado.md) del objeto **Stream** de destino para permitir la conversión de un juego de caracteres a otro. Además, los objetos **Stream** de texto se pueden copiar correctamente a los objetos **Stream** binarios,pero no a lainversa.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

