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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331643"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evitar el uso de IStream:: setSize para extender una secuencia

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Al escribir en secuencias, a veces es necesario agrandarlas porque su tamaño inicial ya no es suficiente. Use el método OLE **IStream:: Write** para lograr esto en lugar de **IStream:: setSize**. **IStream:: Write** amplía automáticamente la secuencia, lo que hace que * * IStream:: setSize * * no sea necesario. Llamar a **IStream:: Write** sin **IStream:: setSize** puede ser hasta tres veces más rápido que realizar la llamada **setSize** antes de **escribir**.
  

