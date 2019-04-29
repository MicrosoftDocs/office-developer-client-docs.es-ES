---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427741"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero de interfaz a la biblioteca de formularios local. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>Parameters

 _ppfcnt_
  
> contempla Puntero a un puntero a la interfaz de la biblioteca de formularios local.
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los programas de instalación de terceros pueden usar la interfaz en la que se devuelve un puntero para instalar formularios específicos de la aplicación en la biblioteca sin que el programa tenga que iniciar sesión en MAPI. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnMAPIOpenLocalFormContainer  <br/> |MFCMAPI usa el método **MAPIOpenLocalFormContainer** para abrir el contenedor de formulario local para representarlo en una ventana nueva.  <br/> |
   
## <a name="see-also"></a>Ver también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

