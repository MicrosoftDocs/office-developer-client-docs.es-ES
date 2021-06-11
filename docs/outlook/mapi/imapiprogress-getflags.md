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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423646"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve la configuración de marca del objeto de progreso para el nivel de operación en el que se calcula la información de progreso.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [salida] Máscara de bits de marcas que controla el nivel de operación en el que se calcula la información de progreso. Se puede devolver la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> El progreso se calcula para el objeto de nivel superior, el objeto al que llama el cliente para iniciar la operación. Por ejemplo, el objeto de nivel superior de una operación de copia de carpeta es la carpeta que se está copiando. Cuando MAPI_TOP_LEVEL no se establece, el progreso se calcula para un objeto de nivel inferior o subobjeto. En la operación de copia de carpeta, un objeto de nivel inferior es una de las subcarpetas de la carpeta que se está copiando.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El valor de las marcas se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

MAPI permite a los proveedores de servicios diferenciar entre objetos de nivel superior y subobjetos con la marca MAPI_TOP_LEVEL para que todos los objetos implicados en una operación puedan usar la misma implementación [imapiprogress](imapiprogressiunknown.md) para mostrar el progreso. Esto hace que la presentación del indicador continúe sin problemas en una sola dirección positiva. Si se MAPI_TOP_LEVEL marca de acceso determina cómo los proveedores de servicios establecen los demás parámetros en llamadas posteriores al objeto de progreso. 
  
El valor devuelto por **GetFlags** lo establece inicialmente el implementador y posteriormente el proveedor de servicios mediante una llamada al método [IMAPIProgress::SetLimits.](imapiprogress-setlimits.md) 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Inicialice siempre la marca para MAPI_TOP_LEVEL y, a continuación, confíe en los proveedores de servicios para borrarla cuando corresponda. Los proveedores de servicios pueden borrar y restablecer la marca llamando al método **IMAPIProgress::SetLimits.** Para obtener más información acerca de cómo implementar **GetFlags** y los demás métodos **IMAPIProgress,** vea [Implementing a Progress Indicator](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando muestre un indicador de progreso, realice la primera llamada a **IMAPIProgress::GetFlags**. El valor devuelto debe MAPI_TOP_LEVEL, ya que todas las implementaciones inicializan el contenido del parámetro  _lpulFlags_ en este valor. Para obtener más información acerca de la secuencia de llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI usa el **método IMAPIProgress::GetFlags** para determinar qué marcas se establecen. Devuelve MAPI_TOP_LEVEL a menos que se hayan establecido marcas mediante el método **IMAPIProgress::SetLimits.**  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

