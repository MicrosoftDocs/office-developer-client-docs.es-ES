---
title: IUnknown IAttachmentSecurity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326988"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que las soluciones de Microsoft Outlook 2010 y Microsoft Outlook 2013 descubran si los datos adjuntos se consideran no seguros y bloqueados para la visualización y la indización.
  
|||
|:-----|:-----|
|Identificador de interfaz:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Comprueba si los datos adjuntos especificados están bloqueados por Outlook 2010 o Outlook 2013 para su visualización e indización.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las soluciones de Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si hay datos adjuntos bloqueados. Los datos adjuntos bloqueados por Outlook 2010 o Outlook 2013 varían en función de cómo se haya configurado Outlook 2010 o Outlook 2013 y de las directivas que haya aplicado un administrador.
  
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Comprobar que los datos adJuntos están bloqueados](how-to-verify-an-attachment-is-blocked.md)

