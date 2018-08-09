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
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817145"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite que las soluciones de Microsoft Outlook 2010 y Microsoft Outlook 2013 averiguar si se considera como datos adjuntos no seguros y bloqueados para su visualización e indización.
  
|||
|:-----|:-----|
|Identificador de interfaz:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Comprueba si los datos adjuntos especificados está bloqueado por Outlook 2010 o Outlook 2013 para su visualización e indización.  <br/> |
   
## <a name="remarks"></a>Comentarios

Soluciones de Outlook 2010 y Outlook 2013 pueden consultar esta interfaz para ver si se bloquea un dato adjunto. Los datos adjuntos que están bloqueados por Outlook 2010 o Outlook 2013 varían dependiendo de cómo se haya configurado Outlook 2010 o Outlook 2013 y las directivas que se ha aplicado un administrador.
  
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Comprobar si los datos adjuntos están bloqueados](how-to-verify-an-attachment-is-blocked.md)

