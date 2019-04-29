---
title: Información sobre las operaciones de tabla asincrónica
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439572"
---
# <a name="about-asynchronous-table-operations"></a>Información sobre las operaciones de tabla asincrónica
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La interfaz **IMAPITable** incluye tres métodos que funcionan de forma asincrónica y tres métodos para controlar una operación asincrónica. En la siguiente tabla se enumeran estos métodos: 
  
|**Operación asincrónica**|**Método de control asincrónico**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Para recuperar información de estado sobre el tipo de una tabla y la operación actual**
  
- Llame al [IMAPITable:: getStatus](imapitable-getstatus.md). Con **getStatus**, un usuario de tabla puede determinar si la tabla es estática o dinámica, si una operación está en curso o ha finalizado, y si se ha producido un error en una operación completada. Por ejemplo, si un cliente necesita cancelar una operación de ordenación porque está tardando demasiado tiempo, el cliente puede llamar primero a **getStatus** para determinar si, de hecho, se está procesando actualmente una operación de ordenación. A continuación, el cliente puede llamar al método [IMAPITable:: ABORT](imapitable-abort.md) para detenerlo. 
    
**Para suspender la actividad hasta que se complete una tarea asincrónica**
  
- Llame al [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md). Llamar a **WaitForCompletion** permite que la tarea se complete sin interrupciones. 
    
## <a name="see-also"></a>Ver también

- [Tablas MAPI](mapi-tables.md)

