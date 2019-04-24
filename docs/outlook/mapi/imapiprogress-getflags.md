---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270270"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la configuración de la marca del objeto Progress para el nivel de operación en el que se calcula la información del progreso.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> contempla Máscara de máscara de marcadores que controla el nivel de funcionamiento en el que se calcula la información del progreso. Se puede devolver la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> Se está calculando el progreso para el objeto de nivel superior, el objeto al que llama el cliente para comenzar la operación. Por ejemplo, el objeto de nivel superior en una operación de copia de carpeta es la carpeta que se está copiando. Cuando MAPI_TOP_LEVEL no se establece, el progreso se calcula para un objeto o subobjeto de nivel inferior. En la operación de copia de carpetas, un objeto de nivel inferior es una de las subcarpetas de la carpeta que se está copiando.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El valor de flags se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

MAPI permite a los proveedores de servicios diferenciar entre objetos de nivel superior y subobjetos con la marca MAPI_TOP_LEVEL para que todos los objetos involucrados en una operación puedan usar la misma implementación de [método imapiprogress](imapiprogressiunknown.md) para mostrar el progreso. Esto hace que la visualización del indicador se lleve a cabo sin problemas en una dirección positiva única. Si la marca MAPI_TOP_LEVEL está establecida determina el modo en que los proveedores de servicios establecen los otros parámetros en las llamadas posteriores al objeto Progress. 
  
El valor devuelto por **GetFlags** es establecido inicialmente por el implementador y, posteriormente, por el proveedor de servicios mediante una llamada al método [método imapiprogress:: SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Inicialice siempre la marca a MAPI_TOP_LEVEL y, a continuación, use los proveedores de servicios para borrarla cuando corresponda. Los proveedores de servicios pueden borrar y restablecer la marca llamando al método **método imapiprogress:: SetLimits** . Para obtener más información acerca de cómo implementar **GetFlags** y los otros métodos **método imapiprogress** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se muestra un indicador de progreso, la primera vez que llama a una llamada a **método imapiprogress:: GetFlags**. El valor devuelto debe ser MAPI_TOP_LEVEL, ya que todas las implementaciones inicializan el contenido del parámetro _lpulFlags_ en este valor. Para obtener más información acerca de la secuencia de llamadas a un objeto Progress, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: GetFlags  <br/> |MFCMAPI usa el método **método imapiprogress:: GetFlags** para determinar qué marcas se establecen. Devuelve MAPI_TOP_LEVEL a menos que se hayan establecido marcas mediante el método **método imapiprogress:: SetLimits** .  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

