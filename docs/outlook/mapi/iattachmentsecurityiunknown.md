---
title: IAttachmentSecurity IUnknown
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411417"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite Microsoft Outlook 2010 y Microsoft Outlook 2013 soluciones para averiguar si un dato adjunto se considera no seguro y se bloquea para su visualización e indización.
  
|||
|:-----|:-----|
|Identificador de interfaz:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Comprueba si un archivo adjunto especificado está bloqueado Outlook 2010 o Outlook 2013 para ver e indizar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si se bloquean los datos adjuntos. Los datos adjuntos bloqueados por Outlook 2010 o Outlook 2013 varían según cómo se haya configurado Outlook 2010 o Outlook 2013 y las directivas que haya aplicado un administrador.
  
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Comprobar que un archivo adjunto está bloqueado](how-to-verify-an-attachment-is-blocked.md)

