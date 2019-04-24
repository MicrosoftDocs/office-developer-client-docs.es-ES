---
title: IUnknown IPSTOVERRIDEREQ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356983"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Tiene acceso a los recursos de un proveedor de almacenamiento de archivos de carpetas personales (PST).
  
|||
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Proveedor de almacén PST  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Inicia el proceso de desbloqueo de un archivo de carpetas personales (. pst).  <br/> |
   
## <a name="remarks"></a>Comentarios

Es posible que los identificadores de interfaz del controlador de anulación de PST no estén definidos en el archivo de encabezado descargable que tiene actualmente, en cuyo caso los encontrará en el tema sobre [constantes MAPI](mapi-constants.md) y puede copiarlos y agregarlos al código. Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h del kit de desarrollo de software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores. 
  
Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para omitir la Directiva PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Vea también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

