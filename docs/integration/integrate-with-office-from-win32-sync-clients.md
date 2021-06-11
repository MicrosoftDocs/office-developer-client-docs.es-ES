---
title: Integrar con Office desde clientes de sincronización de Win32
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Integrar los clientes de sincronización de Win32 de terceros con las aplicaciones de Office Excel Mobile, PowerPoint Mobile y Word Mobile.
ms.openlocfilehash: 83bc6e4cddc17e539b371999fff620c72c595534
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303139"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a>Integrar con Office desde clientes de sincronización de Win32

Integrar los clientes de sincronización de Win32 de terceros con las aplicaciones de Office Excel Mobile, PowerPoint Mobile y Word Mobile. 
  
Puede integrar la aplicación universal de Windows con clientes Excel Mobile, PowerPoint Mobile y Word Mobile mediante el registro de un proveedor de raíz de sincronización. Este artículo describe los procedimientos recomendados que hay que aplicar para garantizar que los clientes de sincronización de Win32 funcionan bien con aplicaciones Office.
  
Esta integración requiere que el cliente de sincronización de Win32 tenga un motor de sincronización.
  
## <a name="register-as-a-sync-root-provider"></a>Registrarse como un proveedor de raíz de sincronización

A menos que el cliente de sincronización esté registrado como proveedor de raíz de sincronización, Office tratará los archivos de la carpeta de sincronización como trata archivos locales normales. Esto significa que Office proporcionará opciones de "mover a OneDrive" a los usuarios cuando intenten compartir el documento. Para evitar este problema en la sincronización de archivos, debe registrarse como un proveedor de raíz de sincronización. Para obtener información sobre cómo registrarse, consulte [Integrar un proveedor de almacenamiento en la nube](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Integrar la aplicación en el nodo raíz del panel de navegación

Para que el cliente de sincronización de Win32 se muestre como un nodo raíz en el panel de navegación del selector de archivos de Windows y del Explorador de archivos, necesita integrar su aplicación en el nivel raíz. Para obtener información sobre cómo hacerlo, consulte [Integrar un proveedor de almacenamiento en la nube](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Agregar la carpeta de sincronización como una biblioteca de documentos (opcional)

En Office, los usuarios pueden crear documentos en las bibliotecas de documentos con una sola acción. Para agregar la ubicación de sincronización a la biblioteca de documentos, use la [función SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>Vea también
<a name="bk_addresources"> </a>

- [Integración con Office](integrate-with-office.md)
    
- [Integrar con Office desde aplicaciones universales de Windows](integrate-with-office-from-windows-universal-apps.md)
    

