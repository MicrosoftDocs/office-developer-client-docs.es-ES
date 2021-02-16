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
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="4725b-103">Integrar con Office desde clientes de sincronización de Win32</span><span class="sxs-lookup"><span data-stu-id="4725b-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="4725b-104">Integrar los clientes de sincronización de Win32 de terceros con las aplicaciones de Office Excel Mobile, PowerPoint Mobile y Word Mobile.</span><span class="sxs-lookup"><span data-stu-id="4725b-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="4725b-p101">Puede integrar la aplicación universal de Windows con clientes Excel Mobile, PowerPoint Mobile y Word Mobile mediante el registro de un proveedor de raíz de sincronización. Este artículo describe los procedimientos recomendados que hay que aplicar para garantizar que los clientes de sincronización de Win32 funcionan bien con aplicaciones Office.</span><span class="sxs-lookup"><span data-stu-id="4725b-p101">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider. This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="4725b-107">Esta integración requiere que el cliente de sincronización de Win32 tenga un motor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="4725b-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="4725b-108">Registrarse como un proveedor de raíz de sincronización</span><span class="sxs-lookup"><span data-stu-id="4725b-108">Register as a sync root provider</span></span>

<span data-ttu-id="4725b-p102">A menos que el cliente de sincronización esté registrado como proveedor de raíz de sincronización, Office tratará los archivos de la carpeta de sincronización como trata archivos locales normales. Esto significa que Office proporcionará opciones de "mover a OneDrive" a los usuarios cuando intenten compartir el documento. Para evitar este problema en la sincronización de archivos, debe registrarse como un proveedor de raíz de sincronización. Para obtener información sobre cómo registrarse, consulte [Integrar un proveedor de almacenamiento en la nube](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4725b-p102">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files. This means that Office will provide "move to OneDrive" options for users when they attempt to share the document. To avoid this for files you sync, you must register as a sync root provider. For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="4725b-113">Integrar la aplicación en el nodo raíz del panel de navegación</span><span class="sxs-lookup"><span data-stu-id="4725b-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="4725b-p103">Para que el cliente de sincronización de Win32 se muestre como un nodo raíz en el panel de navegación del selector de archivos de Windows y del Explorador de archivos, necesita integrar su aplicación en el nivel raíz. Para obtener información sobre cómo hacerlo, consulte [Integrar un proveedor de almacenamiento en la nube](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4725b-p103">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level. For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="4725b-116">Agregar la carpeta de sincronización como una biblioteca de documentos (opcional)</span><span class="sxs-lookup"><span data-stu-id="4725b-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="4725b-p104">En Office, los usuarios pueden crear documentos en las bibliotecas de documentos con una sola acción. Para agregar la ubicación de sincronización a la biblioteca de documentos, use la [función SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4725b-p104">In Office, users can create documents in their document libraries with a single action. To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4725b-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4725b-119">See also</span></span>
<span data-ttu-id="4725b-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="4725b-120"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="4725b-121">Integración con Office</span><span class="sxs-lookup"><span data-stu-id="4725b-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="4725b-122">Integrar con Office desde aplicaciones universales de Windows</span><span class="sxs-lookup"><span data-stu-id="4725b-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

