---
title: Datos adjuntos OLE de apertura con IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818456"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="84232-103">Datos adjuntos OLE de apertura con IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="84232-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="84232-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84232-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84232-105">Al abrir datos adjuntos objeto OLE, use la interfaz de **IStreamDocfile** en lugar de [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) o [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84232-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="84232-106">**IStreamDocfile** proporciona un acceso directo al objeto mediante almacenamiento estructurado, lo que elimina la necesidad de realizar una operación de copia y reducir la sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="84232-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="84232-107">**IStreamDocfile** es una implementación específica de **IStream** con el contenido del objeto stream que garantiza que se aplicar formato de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="84232-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="84232-108">**IStreamDocfile** se implementa mediante los proveedores de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="84232-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

