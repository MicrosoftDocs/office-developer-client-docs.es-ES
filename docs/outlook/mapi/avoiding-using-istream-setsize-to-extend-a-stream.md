---
title: Evitar el uso de IStreamSetSize para extender una secuencia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428917"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitar el uso de IStream::SetSize para extender una secuencia

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al escribir en secuencias, a veces es necesario ampliarlas porque su tamaño inicial ya no es suficiente. Use el método OLE **IStream::Write** para hacerlo en lugar de **IStream::SetSize**. **IStream::Write** extiende automáticamente la secuencia, lo que hace que ** IStream::SetSize ** no es necesario. Llamar **a IStream::Write** sin **IStream::SetSize** puede ser hasta tres veces más rápido que realizar la llamada **SetSize** antes de **Escribir.**
  

