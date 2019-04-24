---
title: Usar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 98f08432-e86c-cba6-45fd-5a6c94d50aaf
description: 'Última modificación: 3 de julio de 2012'
ms.openlocfilehash: b7c651044ab7f4cad7032db69e157c9a3589bde9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329690"
---
# <a name="using-a-wrapped-pst-store-provider"></a>Usar un proveedor de almacén de archivos PST ajustado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para poder usar un proveedor de almacenamiento de archivos de carpetas personales (PST) ajustado, debe inicializar y configurar el proveedor de almacenamiento de PST ajustado. Una vez configurado el proveedor de almacén de archivos PST ajustado, debe implementar funciones para que MAPI y la cola MAPI puedan iniciar sesión en el proveedor de almacenamiento de mensajes. Para obtener más información acerca de la inicialización y el inicio de sesión en un proveedor de almacén de archivos PST ajustado, vea [inicializar un proveedor de almacén](initializing-a-wrapped-pst-store-provider.md) de archivos PST ajustado e [iniciar sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).
  
La interfaz **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** proporciona implementaciones para tareas que suelen realizar los proveedores de almacenamiento de mensajes. Esta interfaz debe estar ajustada para que funcione el proveedor de almacén de archivos PST ajustado de ejemplo. La función **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** requiere una implementación especial. Todas las demás funciones pueden pasar sus parámetros al objeto ajustado subyacente. 
  
En este tema, la función **IMAPISupport:: OpenProfileSection** se muestra mediante un ejemplo de código del proveedor de almacenamiento PST ajustado del ejemplo. El ejemplo implementa un proveedor de archivos PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [Installing the Sample wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).
  
Cuando termine de usar un proveedor de almacén de archivos PST ajustado, debe apagar correctamente el proveedor de almacén de archivos PST ajustado. Para obtener más información, vea [apagar un proveedor de almacenamiento PST ajustado](shutting-down-a-wrapped-pst-store-provider.md).
  
## <a name="open-profile-section-routine"></a>Rutina de sección de perfil abierto

La función **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** abre una sección del perfil actual. La función requiere un tratamiento especial en la implementación del proveedor de almacén de archivos PST ajustado. Cuando `pgNSTGlobalProfileSectionGuid` se solicita, la función devuelve la sección de perfil que se almacena en la memoria caché. 
  
### <a name="csupportopenprofilesection-example"></a>Ejemplo de CSupport:: OpenProfileSection ()

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

## <a name="see-also"></a>Vea también

- [Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md)
- [Instalación del proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
- [Inicio de sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

