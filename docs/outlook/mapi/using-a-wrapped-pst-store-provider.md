---
title: Uso de un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: e74ccd44797bb5629bfe4f390b099771c6932a9b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566470"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Uso de un proveedor de almacén de archivos PST ajustado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para poder usar un proveedor de almacén de archivo (.pst) de carpetas personales ajustado, debe inicializar y configurar el proveedor de almacén de archivos PST ajustado. Después de configura el proveedor de almacén de archivos PST ajustado, debe implementar las funciones para que MAPI y la cola MAPI pueden iniciar sesión en el proveedor de almacén de mensajes. Para obtener más información acerca de inicializar e inicio de sesión un proveedor de almacén de archivos PST ajustado, vea [inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md) y el [Registro en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).
  
La interfaz de **[IMAPISupport::IUnknown](imapisupportiunknown.md)** proporciona implementaciones para las tareas que se realizan habitualmente por mensaje los proveedores de almacén. Esta interfaz debe ser ajustada para que el proveedor de almacén de PST de ajustado de ejemplo para que funcione. La función **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** requiere la implementación especial. Todas las demás funciones pueden pasar sus parámetros en el objeto subyacente ajustado. 
  
En este tema, se muestra la función **IMAPISupport::OpenProfileSection** mediante el uso de un ejemplo de código desde el proveedor de almacén de archivos PST ajustado de ejemplo. En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
Cuando termine de utilizar un proveedor de almacén de archivos PST ajustado, debe cerrar correctamente el proveedor de almacén de archivos PST ajustado. Para obtener más información, vea [Cerrando hacia abajo un ajustado PST proveedor de almacenamiento](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Abrir rutina de sección de perfil

La función **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** abre una sección del perfil actual. La función requiere un tratamiento especial en la implementación del proveedor de almacén de archivos PST ajustado. Cuando el `pgNSTGlobalProfileSectionGuid` se solicita, la función devuelve la sección de perfil que se almacena en caché. 
  
### <a name="csupportopenprofilesection-example"></a>Ejemplo de CSupport::OpenProfileSection()

```cpp
STDMETHODIMP CSupport::OpenProfileSection( 
    LPMAPIUID lpUid,     
    ULONG ulFlags, 
    LPPROFSECT * lppProfileObj) 
{ 
    Log(true,"CSupport::OpenProfileSection\n"); 
    if (lpUid &&  
        IsEqualMAPIUID(lpUid, (void *)&pbNSTGlobalProfileSectionGuid) &&  
        m_lpProfSect) 
    {      
        // Allow the opening of the Global Section 
        if (m_lpProfSect) 
        { 
            *lppProfileObj = m_lpProfSect; 
            (*lppProfileObj)->AddRef(); 
            return S_OK; 
        } 
    } 
    return m_pMAPISup->OpenProfileSection(lpUid, ulFlags, lppProfileObj); 
}
```

## <a name="see-also"></a>Recursos adicionales

- [Información sobre el proveedor de almacén de archivos PST ajustado de muestra](about-the-sample-wrapped-pst-store-provider.md)
- [Instalar la muestra de proveedor de almacén de archivos PST ajustado](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
- [Iniciar sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

