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
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816503"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Evite usar IStream::SetSize para extender una secuencia

  
  
**Hace referencia a**: Outlook 
  
Al escribir en secuencias, en ocasiones, es necesario ampliar ellos porque su tamaño inicial ya no es suficiente. Usar el método OLE **IStream::Write** para hacerlo en lugar de **IStream:: SetSize**. **IStream::Write** extiende automáticamente la secuencia, realizar ** IStream:: SetSize ** innecesarios. Al llamar a **IStream::Write** sin **IStream:: SetSize** puede ser más rápido que hacer el **SetSize** llamada antes de **escribir**hasta tres veces.
  

