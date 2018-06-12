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
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Datos adjuntos OLE de apertura con IStreamDocfile

**Se aplica a**: Outlook 
  
Al abrir datos adjuntos objeto OLE, use la interfaz de **IStreamDocfile** en lugar de [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) o [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile** proporciona un acceso directo al objeto mediante almacenamiento estructurado, lo que elimina la necesidad de realizar una operación de copia y reducir la sobrecarga. **IStreamDocfile** es una implementación específica de **IStream** con el contenido del objeto stream que garantiza que se aplicar formato de almacenamiento estructurado. **IStreamDocfile** se implementa mediante los proveedores de almacén de mensajes. 
  

