---
title: Mode (propiedad, ADO)
TOCTitle: Mode Property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d258623756b53a82c06320185f9b75247087b2d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483323"
---
# <a name="mode-property-ado"></a><span data-ttu-id="a5822-102">Mode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="a5822-102">Mode Property (ADO)</span></span>


<span data-ttu-id="a5822-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5822-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a5822-104">Indica los permisos disponibles para modificar datos de un objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md) o [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a5822-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a5822-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="a5822-105">Settings and Return Values</span></span>

<span data-ttu-id="a5822-p101">Establece o devuelve un valor de tipo [ConnectModeEnum](connectmodeenum.md). El valor predeterminado de **Connection** es **adModeUnknown**, el de **Record** es **adModeRead** y el de un objeto **Stream** asociado a un origen subyacente (abierto con una dirección URL como origen o como el objeto **Stream** predeterminado de **Record**) es **adModeRead**. El valor predeterminado de un objeto **Stream** no asociado a un origen subyacente (con una instancia en memoria) es **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a5822-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5822-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5822-111">Remarks</span></span>

<span data-ttu-id="a5822-p102">Use la propiedad **Mode** para establecer o devolver los permisos de acceso utilizados por el proveedor en la conexión actual. La propiedad **Mode** solo se puede establecer cuando el objeto **Connection** está cerrado.</span><span class="sxs-lookup"><span data-stu-id="a5822-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="a5822-p103">En un objeto **Stream**, si no se ha especificado el modo de acceso, se hereda del origen utilizado para abrir el objeto **Stream**. Por ejemplo, si se abre un objeto **Stream** desde un objeto **Record**, se abre de forma predeterminada del mismo modo que el objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="a5822-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="a5822-116">Esta propiedad es de lectura y escritura mientras el objeto está cerrado y de sólo lectura mientras está abierto.</span><span class="sxs-lookup"><span data-stu-id="a5822-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="a5822-117">**Uso de servicio de datos remotos** Cuando se usa en un objeto Connection de cliente, la propiedad **Mode** sólo puede establecerse en el **valor adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a5822-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>
