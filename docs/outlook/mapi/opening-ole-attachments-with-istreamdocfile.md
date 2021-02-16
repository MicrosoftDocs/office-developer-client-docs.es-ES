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
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Abrir datos adjuntos de OLE con IStreamDocfile

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al abrir datos adjuntos de un objeto OLE, use la **interfaz IStreamDocfile** en lugar de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) o [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx). 

**IStreamDocfile proporciona** acceso directo al objeto mediante almacenamiento estructurado, lo que elimina la necesidad de realizar una operación de copia y reduce la sobrecarga. **IStreamDocfile** es una implementación específica de **IStream** con el contenido de la secuencia que se garantiza que tenga el formato de almacenamiento estructurado. **IStreamDocfile** lo implementan los proveedores de al almacenamiento de mensajes. 
  

