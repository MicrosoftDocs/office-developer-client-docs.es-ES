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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411179"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Incrementa el recuento de referencias de subsistema MAPI e inicializa los datos globales de la DLL MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parameters

 _lpMapiInit_
  
> [in] Puntero a una [MAPIINIT_0](mapiinit_0.md) estructura. El  _parámetro lpMapiInit_ se puede establecer en NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El subsistema MAPI se inicializó correctamente.
    
## <a name="remarks"></a>Comentarios

La **función MAPIInitialize** incrementa el recuento de referencias MAPI para el subsistema MAPI y la función [MAPIUninitialize](mapiuninitialize.md) disminuye el recuento de referencias internas. Por lo tanto, el número de llamadas a una función debe ser igual al número de llamadas a la otra. **MAPIInitialize** devuelve S_OK si MAPI no se ha inicializado previamente. 
  
Un cliente o proveedor de servicios debe llamar **a MAPIInitialize antes** de realizar cualquier otra llamada MAPI. Si no lo hace, las llamadas de cliente o proveedor de servicios devuelven el MAPI_E_NOT_INITIALIZED valor. 
  
Al llamar a **MAPIInitialize** desde una aplicación multiproceso, establezca el parámetro  _lpMapiInit_ en una [estructura](mapiinit_0.md) MAPIINIT_0 que se declara de la siguiente manera: 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
y llama a: 
  
 **MAPIInitialize** ( &amp; MAPIINIT); 
  
Cuando se declara esta estructura, MAPI crea un subproceso independiente para controlar la ventana de notificación, que continúa hasta que el recuento de referencias de inicialización cae a cero. Un Windows debe establecer el **miembro ulflags** de la **estructura MAPIINIT_0** apuntada por _lpMapiInit_ en MAPI_NT_SERVICE. 
  
> [!NOTE]
> No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función **DllMain** de Win32 o cualquier otra función que cree o termine subprocesos. Para obtener más información, vea [Using Thread-Safe Objects](using-thread-safe-objects.md). 
  
 **MAPIInitialize** no devuelve ninguna información de error extendida. A diferencia de la mayoría de las demás llamadas MAPI, los significados de sus valores devueltos están estrictamente definidos para corresponder al paso concreto de la inicialización que ha fallado: 
  
1. Comprueba los parámetros y las marcas.
    
    MAPI_E_INVALID_PARAMETER o MAPI_E_UNKNOWN_FLAGS. El autor de la llamada ha pasado un parámetro o una marca no válidos.
    
2. Inicializa las claves del Registro necesarias para MAPI y confirma el tipo de sistema operativo. Este paso solo se produce si el proceso de cliente se ejecuta como un servicio en Windows y establece el MAPI_NT service en la **MAPIINIT_0** estructura. 
    
    MAPI_E_TOO_COMPLEX. El proceso de llamada es un Windows y las claves del Registro requeridas por MAPI no se pudieron inicializar. 
    
    Es posible que haya información adicional disponible en el registro de eventos de la aplicación.
    
3. Compruebe la compatibilidad de MAPI con OLE y, a continuación, inicialice OLE.
    
1. Comprueba la compatibilidad entre las versiones actuales de OLE y MAPI. 
    
    MAPI_E_VERSION. La versión de OLE instalada en la estación de trabajo no es compatible con esta versión de MAPI.
    
2. Inicializa OLE. 
    
    Solo durante este paso, esta función puede devolver un código de error que no aparece aquí. Cualquier error  _que_ no aparezca aquí debe asumirse que procede de la función OLE **CoInitialize**.
    
4. Inicializa variables globales por proceso.
    
    MAPI_E_SESSION_LIMIT. MAPI configura el contexto específico del proceso actual. Los errores pueden producirse en Win16 si el número de procesos supera un número determinado o en cualquier sistema si se agota la memoria disponible.
    
5. Inicializa variables globales compartidas de todos los procesos.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. No había suficientes recursos del sistema disponibles para completar la operación.
    
6. Inicializa el motor de notificaciones, crea su ventana y su subproceso si la marca MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Puede producirse un error si se agotan los recursos del sistema. 
    
7. Carga e inicializa el proveedor de perfiles. Comprueba que **MAPIInitialize** puede tener acceso a la clave del Registro donde se almacenan los datos de perfil. 
    
    MAPI_E_NOT_INITIALIZED. El proveedor de perfiles ha encontrado un error. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI usa el **método MAPIInitialize** para inicializar MAPI en un subproceso en segundo plano para realizar algún procesamiento de tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

