---
title: IPSTOVERRIDEREQ IUnknown
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389109"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Proveedor de almacén de recursos de acceso de un archivo de carpetas personales (PST).
  
|||
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Proveedor de almacén de archivos PST  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |Inicia el procedimiento de desbloqueo para un archivo de carpetas personales (.pst).  <br/> |
   
## <a name="remarks"></a>Comentarios

Los identificadores de interfaz de controlador de invalidar PST no puede definirse en el archivo de encabezado que se pueden descargar que tiene actualmente, en cuyo caso se encontrarlos en el tema de [Las constantes de MAPI](mapi-constants.md) y puede copiar y agregarlos a su código. Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores. 
  
Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Vea también



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

