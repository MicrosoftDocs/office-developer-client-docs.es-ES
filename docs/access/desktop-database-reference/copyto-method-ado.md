---
title: CopyTo (método, ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bd949b92068619b76ac78d5e62cde0e247ed7b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484748"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="88387-102">CopyTo (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="88387-102">CopyTo Method (ADO)</span></span>


<span data-ttu-id="88387-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88387-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="88387-104">Copia el número especificado de caracteres o bytes (según [Type](type-property-ado-stream.md)) de un objeto [Stream](stream-object-ado.md) a otro objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="88387-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88387-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88387-105">Syntax</span></span>

<span data-ttu-id="88387-106">*Secuencia*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="88387-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="88387-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88387-107">Parameters</span></span>

  - <span data-ttu-id="88387-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="88387-108">*DestStream*</span></span>

  - <span data-ttu-id="88387-p101">Valor de variable de objeto que contiene una referencia a un objeto **Stream** abierto. El actual objeto **Stream** se copia en el objeto **Stream** de destino especificado por *DestStream*. El objeto **Stream** de destino ya debe estar abierto. De lo contrario, se produce un error en tiempo de ejecución.

</span><span class="sxs-lookup"><span data-stu-id="88387-p101">An object variable value that contains a reference to an open **Stream** object. The current **Stream** is copied to the destination **Stream** specified by *DestStream*. The destination **Stream** must already be open. If not, a run-time error occurs.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="88387-113">El parámetro <EM>DestStream</EM> puede no ser un proxy del objeto <STRONG>Stream</STRONG> porque esto requiere acceso a una interfaz privada en el objeto <STRONG>Stream</STRONG> que no puede ser remoto para el cliente.</span><span class="sxs-lookup"><span data-stu-id="88387-113">The <EM>DestStream</EM> parameter may not be a proxy of <STRONG>Stream</STRONG> object because this requires access to a private interface on the <STRONG>Stream</STRONG> object that cannot be remoted to the client.</span></span></P>



  - <span data-ttu-id="88387-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="88387-114">*NumChars*</span></span>

  - <span data-ttu-id="88387-115">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="88387-115">Optional.</span></span> <span data-ttu-id="88387-116">Valor de tipo **Integer** que especifica el número de bytes o caracteres que se van a copiar a partir de la actual posición en el objeto **Stream** de origen al objeto **Stream** de destino.</span><span class="sxs-lookup"><span data-stu-id="88387-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="88387-117">El valor predeterminado es – 1, que especifica que todos los caracteres o bytes se copian desde la posición actual hasta [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="88387-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="88387-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88387-118">Remarks</span></span>

<span data-ttu-id="88387-119">Este método copia el número especificado de caracteres o bytes, a partir de la actual posición especificada por la propiedad [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="88387-119">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property.</span></span> <span data-ttu-id="88387-120">Si el número especificado es mayor que el número de bytes disponibles hasta **EOS**, sólo se copiarán los caracteres o bytes desde la posición actual hasta **EOS**.</span><span class="sxs-lookup"><span data-stu-id="88387-120">If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied.</span></span> <span data-ttu-id="88387-121">Si el valor de *NumChars* es – 1 o se omite, se copiarán todos los caracteres o bytes a partir de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="88387-121">If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="88387-p104">Si hay caracteres o bytes en la secuencia de destino, se mantiene todo el contenido situado más allá del punto donde finaliza la copia y no se ve truncado. El valor de **Position** será el byte inmediatamente después del último byte copiado. Si desea truncar estos bytes, llame a [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="88387-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="88387-p105">**CopyTo** debe utilizarse para copiar datos a un objeto **Stream** de destino del mismo tipo que el objeto **Stream** de origen (el valor de la propiedad **Type** de ambos objetos debe ser **adTypeText** o **adTypeBinary**). Para los objetos **Stream** de texto, puede cambiar la configuración de la propiedad [Charset](charset-property-ado.md) del objeto **Stream** de destino para permitir la conversión de un juego de caracteres a otro. Además, los objetos **Stream** de texto se pueden copiar correctamente a los objetos **Stream** binarios,\*\*\*\* pero no a la\*\*\*\* inversa.</span><span class="sxs-lookup"><span data-stu-id="88387-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

