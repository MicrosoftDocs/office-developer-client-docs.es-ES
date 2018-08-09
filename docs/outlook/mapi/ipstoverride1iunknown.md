---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817944"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite a un proveedor de almacén de carpetas personales (PST) de archivo invalidar la directiva PSTDisableGrow.
  
|||
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Se implementa mediante:  <br/> |Proveedor de almacén de archivos PST  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Recupera la lista de registros para el archivo de carpetas personales (.pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registra los archivos de carpetas personales para el desbloqueo automático, evitar más llamadas a HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Desbloquea un archivo de carpetas personales para el crecimiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los identificadores de interfaz de controlador de invalidar PST no puede definirse en el archivo de encabezado que se pueden descargar que tiene actualmente, en cuyo caso se encontrarlos en el tema de [Las constantes de MAPI](mapi-constants.md) y puede copiar y agregarlos a su código. Use la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows para asociar los nombres simbólicos de identificador único global (GUID) con sus valores. 
  
Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para que omita la directiva de PSTDisableGrow en Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Vea también



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

