---
title: IUnknown IPSTOVERRIDE1
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
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315501"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que un proveedor del almacén de archivos de carpetas personales (PST) invalide la Directiva PSTDisableGrow.
  
|||
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |Proveedor de almacén PST  <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Identificador de interfaz:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |Recupera la lista de registros del archivo de carpetas personales (. pst).  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |Registra los archivos de carpetas personales para el desbloqueo automático, evitando más llamadas a HrTrustedPSTOverrideHandlerCallback.  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |Desbloquea un archivo de carpetas personales para el crecimiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Es posible que los identificadores de interfaz del controlador de anulación de PST no estén definidos en el archivo de encabezado descargable que tiene actualmente, en cuyo caso los encontrará en el tema sobre [constantes MAPI](mapi-constants.md) y puede copiarlos y agregarlos al código. Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h del kit de desarrollo de software (SDK) de Microsoft Windows para asociar nombres simbólicos de identificador único global (GUID) con sus valores. 
  
Para obtener más información, vea [cómo implementar un controlador de reemplazo de PST para omitir la Directiva PSTDisableGrow en Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Vea también



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

