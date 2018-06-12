---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818267"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Se aplica a**: Outlook 
  
Incrementa el recuento de referencia del subsistema MAPI e inicializa datos globales para la DLL de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Sintaxis

 _lpMapiInit_
  
> [entrada] Puntero a una estructura [MAPIINIT_0](mapiinit_0.md) . El parámetro _lpMapiInit_ se puede establecer en NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El subsistema MAPI se inicializó correctamente.
    
## <a name="remarks"></a>Notas

Los incrementos de función **MAPIInitialize** contar la referencia MAPI para el subsistema MAPI y el disminuye de función [MAPIUninitialize](mapiuninitialize.md) el interno recuento de referencia. Por lo tanto, el número de llamadas a una función debe ser igual que el número de llamadas a otro. **MAPIInitialize** devuelve S_OK si MAPI no se ha inicializado anteriormente. 
  
Un proveedor de servicio o cliente debe llamar **MAPIInitialize** antes de realizar cualquier otra llamada MAPI. Si no lo hace que las llamadas de cliente o servicio proveedor devolver el valor MAPI_E_NOT_INITIALIZED. 
  
Cuando se llama a **MAPIInitialize** desde una aplicación multiproceso, establezca el parámetro _lpMapiInit_ en una estructura [MAPIINIT_0](mapiinit_0.md) que se declara del siguiente modo: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
y la llamada: 
  
 **MAPIInitialize** (&amp;MAPIINIT); 
  
Cuando se declara esta estructura, MAPI crea un subproceso independiente para controlar la ventana de notificación, que continúa hasta que el recuento de referencia initialize entra en cero. Un servicio de Windows debe establecer al miembro **ulflags** de la estructura **MAPIINIT_0** que señala _lpMapiInit_ a MAPI_NT_SERVICE. 
  
> [!NOTE]
> No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función de Win32 **DllMain** o cualquier otra función que crea o termina subprocesos. Para obtener más información, vea [Uso de objetos de subprocesos](using-thread-safe-objects.md). 
  
 **MAPIInitialize** no devuelve ninguna información de error extendido. A diferencia de la mayoría de llamadas MAPI, el significado de sus valores devueltos se define estrictamente para que se correspondan con el paso concreto de la inicialización con errores: 
  
1. Comprueba los parámetros y los indicadores.
    
    MAPI_E_INVALID_PARAMETER o MAPI_E_UNKNOWN_FLAGS. Se pasó un parámetro no válido o marca.
    
2. Inicializa las claves del registro necesarias para MAPI y confirma el tipo de sistema operativo. Este paso sólo ocurre si el proceso de cliente se ejecuta como un servicio en Windows y establece la marca de servicio de MAPI_NT en la estructura **MAPIINIT_0** . 
    
    MAPI_E_TOO_COMPLEX. El proceso de llamada es un servicio de Windows y no se podrían inicializar las claves del registro necesarias para MAPI. 
    
    Información adicional puede estar disponible en el registro de eventos de aplicación.
    
3. Comprobar la compatibilidad de MAPI con OLE y, a continuación, inicializar OLE.
    
1. Comprobaciones para la compatibilidad entre las versiones actuales de OLE y MAPI. 
    
    MAPI_E_VERSION. La versión de OLE instalada en la estación de trabajo no es compatible con esta versión de MAPI.
    
2. Inicializa OLE. 
    
    Durante este paso solo, esta función puede devolver un código de error no se muestran aquí. Cualquier error _no_ aparece aquí se supone que debe proceder de la función OLE **CoInitialize**.
    
4. Inicializa las variables globales por proceso.
    
    MAPI_E_SESSION_LIMIT. MAPI configura contexto específica para el proceso actual. Es posible que se producen errores en Win16 si el número de procesos supera un cierto número, o en cualquier sistema si se ha agotado la memoria disponible.
    
5. Inicializa shared variables globales de todos los procesos.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. No hay suficientes recursos del sistema estaban disponibles para completar la operación.
    
6. Inicializa el motor de notificación, crea su ventana y su subproceso si solicitado por el indicador MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Puede producirse un error si se agotan los recursos del sistema. 
    
7. Carga e inicializa el proveedor de perfiles. Comprueba que **MAPIInitialize** puede obtener acceso a la clave del registro donde se almacenan los datos de perfil. 
    
    MAPI_E_NOT_INITIALIZED. El proveedor de perfiles detectó un error. 
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI, utiliza el método **MAPIInitialize** para inicializar MAPI en un subproceso en segundo plano para realizar algún procesamiento de tabla.  <br/> |
   
## <a name="see-also"></a>Ver también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

