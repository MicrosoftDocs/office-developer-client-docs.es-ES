---
title: Acerca de las operaciones asincrónicas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816349"
---
# <a name="about-asynchronous-table-operations"></a>Acerca de las operaciones asincrónicas de tabla
 
**Hace referencia a**: Outlook 
  
La interfaz **IMAPITable** incluye tres métodos que operan de forma asincrónica y tres métodos para controlar una operación asincrónica. En la siguiente tabla se enumera estos métodos: 
  
|**Operación asincrónica**|**Método de control asincrónico**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Para recuperar información de estado sobre el tipo y la operación actual de una tabla**
  
- Llame a [IMAPITable::GetStatus](imapitable-getstatus.md). Con **GetStatus**, un usuario de la tabla puede determinar si la tabla es estático o dinámico, si una operación está en curso o ha finalizado y si se ha producido un error de una operación completada. Por ejemplo, si un cliente necesita cancelar una operación de ordenación porque se está tardando demasiado tiempo, el cliente puede llamar primero **GetStatus** para determinar si, en realidad, una operación de ordenación es actualmente el procesamiento. A continuación, el cliente puede llamar a [IMAPITable::Abort](imapitable-abort.md) para que deje. 
    
**Para suspender la actividad hasta que haya finalizado una tarea asincrónica**
  
- Llame a [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). Una llamada a **WaitForCompletion** permite la tarea se complete sin interrupciones. 
    
## <a name="see-also"></a>Vea también

- [Tablas MAPI](mapi-tables.md)

