---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414650"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de perfiles, una tabla que contiene información sobre todos los perfiles disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Siempre NULL.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de perfiles.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de perfiles se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::GetProfileTable** proporciona acceso a la tabla de perfiles, que contiene una fila por cada perfil disponible. Solo hay dos columnas en cada fila: el nombre para mostrar del perfil y una marca que indica si el perfil es el predeterminado. 
  
Los perfiles que se han eliminado o que están en uso pero que se han marcado para su eliminación, no se incluyen en la tabla de perfiles. La tabla de perfiles es estática; Las adiciones y eliminaciones posteriores de perfiles no se reflejan en la tabla. 
  
Si no existen perfiles, **GetProfileTable** devuelve una tabla con cero filas. 
  
Para obtener más información acerca de la tabla de perfiles, vea [Tablas de perfiles](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI usa el **método IProfAdmin::GetProfileTable** para que la tabla de perfiles se muestre en un nuevo cuadro de diálogo.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

