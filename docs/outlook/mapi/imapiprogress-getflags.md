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
ms.openlocfilehash: 9a5e4205a808c7a6e469d2e9cb0a1b3c17a92d21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573547"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve marca configuración desde el objeto de progreso para el nivel de operación en la que se calcula la información de progreso.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [out] Una máscara de bits de indicadores que controla el nivel de operación en progreso que se calcula de la información. Se puede devolver la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> Progreso se que se calcula para el objeto de nivel superior, el objeto que se llama por el cliente a comenzar la operación. Por ejemplo, el objeto de nivel superior en una operación de copia de la carpeta es la carpeta que se va a copiar. Cuando no se establece MAPI_TOP_LEVEL, progreso se calcula para un objeto de nivel inferior o subobjetos. En la operación de copia de la carpeta, un objeto de nivel inferior es una de las subcarpetas en la carpeta que se va a copiar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El valor de flags se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

MAPI permite a los proveedores de servicio diferenciar entre objetos de nivel superior y subobjetos con el indicador MAPI_TOP_LEVEL para que todos los objetos implicados en una operación pueden usar la misma implementación de [IMAPIProgress](imapiprogressiunknown.md) para mostrar el progreso. Esto hace que la visualización del indicador se realice correctamente en un solo sentido positivo. Si se establece la marca MAPI_TOP_LEVEL determina cómo los proveedores de servicios establecen los demás parámetros en llamadas posteriores al objeto de progreso. 
  
El valor devuelto por **GetFlags** se establece inicialmente el implementador y posteriormente por el proveedor de servicios a través de una llamada al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Inicializar siempre la marca a MAPI_TOP_LEVEL y, a continuación, se basan en proveedores de servicios para desactivarla cuando sea apropiado. Proveedores de servicios pueden borrar y restablecer el indicador llamando al método **IMAPIProgress::SetLimits** . Para obtener más información acerca de cómo implementar **GetFlags** y los otros métodos de **IMAPIProgress** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se muestra un indicador de progreso, realizar su primera llamada a una llamada a **IMAPIProgress::GetFlags**. El valor devuelto debe ser MAPI_TOP_LEVEL, debido a que todas las implementaciones de inicialización el contenido del parámetro _lpulFlags_ para este valor. Para obtener más información acerca de la secuencia de llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI usa el método **IMAPIProgress::GetFlags** para determinar qué marcas se establecen. Devuelve MAPI_TOP_LEVEL a menos que se han configurado indicadores mediante el método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

