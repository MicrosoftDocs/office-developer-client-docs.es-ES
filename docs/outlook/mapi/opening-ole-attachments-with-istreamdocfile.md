---
title: Abrir datos adjuntos de OLE con IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326232"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="ddba4-103">Abrir datos adjuntos de OLE con IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="ddba4-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="ddba4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddba4-105">Al abrir los datos adjuntos de un objeto OLE, use la **interfaz IStreamDocfile** en lugar de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) o [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddba4-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="ddba4-106">**IStreamDocfile** proporciona acceso directo al objeto mediante almacenamiento estructurado, lo que elimina la necesidad de realizar una operación de copia y reduce la sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="ddba4-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="ddba4-107">**IStreamDocfile** es una implementación específica de **IStream** con el contenido de la secuencia con el formato garantizado como almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="ddba4-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="ddba4-108">Los proveedores de almacén de mensajes implementan **IStreamDocfile.**</span><span class="sxs-lookup"><span data-stu-id="ddba4-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

