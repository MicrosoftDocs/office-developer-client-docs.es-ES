---
title: Charset (propiedad, ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703982"
---
# <a name="charset-property-ado"></a><span data-ttu-id="fbc75-102">Charset (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="fbc75-102">Charset property (ADO)</span></span>


<span data-ttu-id="fbc75-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbc75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbc75-104">Indica el juego de caracteres al que debe convertirse el contenido de un objeto [Stream](stream-object-ado.md) de texto para su almacenamiento en el búfer interno de objetos Stream.</span><span class="sxs-lookup"><span data-stu-id="fbc75-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fbc75-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="fbc75-105">Settings and return values</span></span>

<span data-ttu-id="fbc75-106">Establece o devuelve un valor de tipo **String** que especifica el juego de caracteres al que se va a convertir el contenido del objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="fbc75-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="fbc75-107">El valor predeterminado es "Unicode".</span><span class="sxs-lookup"><span data-stu-id="fbc75-107">The default value is "Unicode".</span></span> <span data-ttu-id="fbc75-108">Los valores permitidos son cadenas típicas que se pasan a través de la interfaz como cadenas de juegos de caracteres de Internet (por ejemplo, "iso-8859-1", "Windows-1252", etc.).</span><span class="sxs-lookup"><span data-stu-id="fbc75-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="fbc75-109">Para obtener una lista de las cadenas de conjunto de caracteres que se conoce por un sistema, vea las subclaves de HKEY\_clases\_raíz\\MIME\\base de datos\\Charset en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="fbc75-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc75-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbc75-110">Remarks</span></span>

<span data-ttu-id="fbc75-p102">En un objeto **Stream** de texto, los datos se almacenan en el juego de caracteres especificado por la propiedad **Charset**. El valor predeterminado es Unicode. La propiedad **Charset** se utiliza para convertir los datos que entran en el objeto **Stream** o que salen del objeto **Stream**. Por ejemplo, si el objeto **Stream** contiene datos ISO-8859-1 y esos datos se copian en una cadena BSTR, el objeto **Stream** convertirá los datos a Unicode, y viceversa.</span><span class="sxs-lookup"><span data-stu-id="fbc75-p102">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property. The default is Unicode. The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**. For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode. The reverse is also true.</span></span>

<span data-ttu-id="fbc75-116">En el caso de un objeto **Stream** abierto, el valor de [Position](position-property-ado.md) actual debe indicar una posición situada al comienzo del objeto **Stream** (0) para que se pueda establecer el valor de **Charset**.</span><span class="sxs-lookup"><span data-stu-id="fbc75-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="fbc75-p103">**Charset** se utiliza únicamente con objetos **Stream** de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se omite si el valor de **Type** es **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="fbc75-p103">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

