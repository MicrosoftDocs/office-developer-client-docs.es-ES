---
title: Integración con Office desde aplicaciones de iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office para iOS proporciona una solución extensible que permite la integración con aplicaciones de terceros. Este artículo describe cómo se puede realizar la integración con Office desde una aplicación de iOS pasando los usuarios desde la aplicación a Office y, a continuación, devolviéndolos a la aplicación.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413853"
---
# <a name="integrate-with-office-from-ios-applications"></a><span data-ttu-id="24d39-104">Integración con Office desde aplicaciones de iOS</span><span class="sxs-lookup"><span data-stu-id="24d39-104">Integrate with Office from iOS applications</span></span>

<span data-ttu-id="24d39-p102">Office para iOS proporciona una solución extensible que permite la integración con aplicaciones de terceros. Este artículo describe cómo se puede realizar la integración con Office desde una aplicación de iOS pasando los usuarios desde la aplicación a Office y, a continuación, devolviéndolos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24d39-p102">Office for iOS provides an extensible solution that enables integration with third-party applications. This article describes how you can integrate with Office from your iOS application by passing users from your application to Office, and then returning them to your application.</span></span>
  
<span data-ttu-id="24d39-p103">Puede permitir que los usuarios que ejecutan Office en un dispositivo iOS abran y editen archivos almacenados en SharePoint o en OneDrive desde cualquier aplicación y, a continuación, devolverlos rápidamente a la aplicación original cuando hayan terminado de editar el archivo. Para ello, pasa los archivos a Office a través de controladores de protocolo y se asegura de que la invocación a Office se realiza de una forma que Office pueda entender.</span><span class="sxs-lookup"><span data-stu-id="24d39-p103">You can enable users who are running Office on an iOS device to open and edit files stored in SharePoint or OneDrive from any application, and then quickly return them to the original application when they're done editing the file. To do this, you pass files to Office via protocol handlers, and you make sure that Office is invoked in a way that Office can understand.</span></span>
  
<span data-ttu-id="24d39-109">Cuando un usuario ha terminado de editar un archivo, puede elegir la flecha atrás en la aplicación de Office para cerrar el documento y regresar a la aplicación de almacenamiento original, siempre que usted pase información específica a la aplicación de Office cuando esta se inicia.</span><span class="sxs-lookup"><span data-stu-id="24d39-109">When a user is done editing a file, they can choose the back arrow in the Office application to close the document and return to the original storage application, provided you pass specific information to the Office application when it launches.</span></span>
  
## <a name="verify-that-office-has-been-installed"></a><span data-ttu-id="24d39-110">Comprobar que Office está instalado</span><span class="sxs-lookup"><span data-stu-id="24d39-110">Verify that Office has been installed</span></span>

<span data-ttu-id="24d39-p104">La aplicación de referencia deberá comprobar primero que una determinada aplicación de Office está instalada. Las siguientes aplicaciones de Office se pueden instalar en dispositivos iOS para la visualización y edición de documentos:</span><span class="sxs-lookup"><span data-stu-id="24d39-p104">Your referring application will first need to verify that a particular Office application is installed. The following Office applications can be installed on iOS devices for document viewing and editing:</span></span>
  
- <span data-ttu-id="24d39-113">Excel</span><span class="sxs-lookup"><span data-stu-id="24d39-113">Excel</span></span>
    
- <span data-ttu-id="24d39-114">OneNote</span><span class="sxs-lookup"><span data-stu-id="24d39-114">OneNote</span></span>
    
- <span data-ttu-id="24d39-115">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="24d39-115">PowerPoint</span></span>
    
- <span data-ttu-id="24d39-116">Word</span><span class="sxs-lookup"><span data-stu-id="24d39-116">Word</span></span>
    
<span data-ttu-id="24d39-p105">Use el método [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) para determinar si la aplicación puede abrir el recurso. Este método toma la dirección URL para el recurso como un parámetro y devuelve **No** si la aplicación que acepta la dirección URL no está disponible. Si **canOpenURL** devuelve **No**, deberá solicitar al usuario que instale Office.</span><span class="sxs-lookup"><span data-stu-id="24d39-p105">Use the [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) method to determine whether your application can open the resource. This method takes the URL for the resource as a parameter, and returns **No** if the application that accepts the URL is not available. If **canOpenURL** returns **No**, you'll need to prompt the user to install Office.</span></span>
  
### <a name="prompt-the-user-to-install-office"></a><span data-ttu-id="24d39-120">Solicitar al usuario que instale Office</span><span class="sxs-lookup"><span data-stu-id="24d39-120">Prompt the user to install Office</span></span>

 <span data-ttu-id="24d39-p106">Si una determinada aplicación de Office no está instalada, puede usar un objeto [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) para representar la tienda de aplicaciones de iTunes en su aplicación y mostrar al usuario la aplicación de Office que debe instalar. La siguiente tabla enumera los identificadores de iTunes que se deben usar para invocar cada una de las aplicaciones de Office en el controlador de vistas de productos del Store Kit.</span><span class="sxs-lookup"><span data-stu-id="24d39-p106">If a particular Office application is not installed, you can use an [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) object to render the iTunes app store in your application and show the user the Office application to install. The following table lists the iTunes identifier to use to invoke each Office application in the Store Kit Product View Controller.</span></span> 
  
|<span data-ttu-id="24d39-123">**Aplicación de Office**</span><span class="sxs-lookup"><span data-stu-id="24d39-123">**Office application**</span></span>|<span data-ttu-id="24d39-124">**Identificador de iTunes**</span><span class="sxs-lookup"><span data-stu-id="24d39-124">**iTunes identifier**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24d39-125">Excel</span><span class="sxs-lookup"><span data-stu-id="24d39-125">Excel</span></span>  <br/> |[<span data-ttu-id="24d39-126"> https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="24d39-126">https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="24d39-127">OneNote (iPhone)</span><span class="sxs-lookup"><span data-stu-id="24d39-127">OneNote (iPhone)</span></span>  <br/> |[<span data-ttu-id="24d39-128"> https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="24d39-128">https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="24d39-129">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="24d39-129">PowerPoint</span></span>  <br/> |[<span data-ttu-id="24d39-130"> https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="24d39-130">https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|<span data-ttu-id="24d39-131">Word</span><span class="sxs-lookup"><span data-stu-id="24d39-131">Word</span></span>  <br/> |[<span data-ttu-id="24d39-132"> https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span><span class="sxs-lookup"><span data-stu-id="24d39-132">https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4</span></span>](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a><span data-ttu-id="24d39-133">Invocar a Office</span><span class="sxs-lookup"><span data-stu-id="24d39-133">Invoke Office</span></span>

<span data-ttu-id="24d39-134">Cuando la aplicación de Office está instalada, la aplicación de referencia puede invocar a Office pasando los siguientes detalles:</span><span class="sxs-lookup"><span data-stu-id="24d39-134">When the Office application is installed, your referring application can invoke Office by passing the following details:</span></span> 
  
- <span data-ttu-id="24d39-135">Protocolo de Office</span><span class="sxs-lookup"><span data-stu-id="24d39-135">Office protocol</span></span>
    
- <span data-ttu-id="24d39-136">Modo de apertura</span><span class="sxs-lookup"><span data-stu-id="24d39-136">Open mode</span></span>
    
- <span data-ttu-id="24d39-137">URL</span><span class="sxs-lookup"><span data-stu-id="24d39-137">URL</span></span>
    
- <span data-ttu-id="24d39-138">Protocolo de retorno</span><span class="sxs-lookup"><span data-stu-id="24d39-138">Passback protocol</span></span>
    
- <span data-ttu-id="24d39-139">Contexto del documento</span><span class="sxs-lookup"><span data-stu-id="24d39-139">Document context</span></span>
    
<span data-ttu-id="24d39-140">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-140">Schema format:</span></span>
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
<span data-ttu-id="24d39-141">El siguiente ejemplo muestra una solicitud para invocar un archivo de Word para su edición:</span><span class="sxs-lookup"><span data-stu-id="24d39-141">The following example shows a request to invoke a Word file for editing:</span></span>
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a><span data-ttu-id="24d39-142">Protocolos de Office</span><span class="sxs-lookup"><span data-stu-id="24d39-142">Office protocols</span></span>

<span data-ttu-id="24d39-143">La siguiente tabla enumera los protocolos para cada aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="24d39-143">The following table lists the protocols for each Office application.</span></span> 
  
|<span data-ttu-id="24d39-144">**Aplicación**</span><span class="sxs-lookup"><span data-stu-id="24d39-144">**Application**</span></span>|<span data-ttu-id="24d39-145">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="24d39-145">**Protocol**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24d39-146">Excel</span><span class="sxs-lookup"><span data-stu-id="24d39-146">Excel</span></span>  <br/> |<span data-ttu-id="24d39-147">ms-excel:</span><span class="sxs-lookup"><span data-stu-id="24d39-147">ms-excel:</span></span>  <br/> |
|<span data-ttu-id="24d39-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="24d39-148">OneNote</span></span>  <br/> |<span data-ttu-id="24d39-149">onenote:</span><span class="sxs-lookup"><span data-stu-id="24d39-149">onenote:</span></span>  <br/> |
|<span data-ttu-id="24d39-150">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="24d39-150">PowerPoint</span></span>  <br/> |<span data-ttu-id="24d39-151">ms-powerpoint:</span><span class="sxs-lookup"><span data-stu-id="24d39-151">ms-powerpoint:</span></span>  <br/> |
|<span data-ttu-id="24d39-152">Word</span><span class="sxs-lookup"><span data-stu-id="24d39-152">Word</span></span>  <br/> |<span data-ttu-id="24d39-153">ms-word:</span><span class="sxs-lookup"><span data-stu-id="24d39-153">ms-word:</span></span>  <br/> |
   
### <a name="open-mode"></a><span data-ttu-id="24d39-154">Modo de apertura</span><span class="sxs-lookup"><span data-stu-id="24d39-154">Open mode</span></span>

<span data-ttu-id="24d39-p107">Las aplicaciones de Office pueden abrir archivos directamente en el modo de visualización (ofv) o edición (ofe). El modo de edición es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="24d39-p107">Office applications can open files directly into view (ofv) or edit (ofe) mode. Edit mode is the default.</span></span> 
  
<span data-ttu-id="24d39-157">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-157">Schema format:</span></span>
  
 `<ofv or ofe>`
  
### <a name="url"></a><span data-ttu-id="24d39-158">URL</span><span class="sxs-lookup"><span data-stu-id="24d39-158">URL</span></span>

<span data-ttu-id="24d39-159">La dirección URL incluye tres partes:</span><span class="sxs-lookup"><span data-stu-id="24d39-159">The URL includes three parts:</span></span> 
  
- <span data-ttu-id="24d39-160">La declaración de que el archivo se abrirá para su edición (ofe)</span><span class="sxs-lookup"><span data-stu-id="24d39-160">The declaration that the file will be opened for edit (ofe)</span></span>
    
- <span data-ttu-id="24d39-161">El descriptor de la dirección URL (|u|)</span><span class="sxs-lookup"><span data-stu-id="24d39-161">The URL descriptor (|u|)</span></span>
    
- <span data-ttu-id="24d39-162">La dirección URL</span><span class="sxs-lookup"><span data-stu-id="24d39-162">The URL</span></span>
    
<span data-ttu-id="24d39-p108">La dirección URL se debe codificar y debe ser un vínculo directo al archivo (no una redirección). Si la dirección URL está en un formato que Office no puede gestionar o simplemente se produce un error en la descarga, Office no devolverá al usuario a la aplicación que realizó la invocación.</span><span class="sxs-lookup"><span data-stu-id="24d39-p108">The URL has to be encoded and must be a direct link to the file (not a redirect). If the URL is in a format that Office cannot handle, or the download simply fails, Office will not return the user to the invoking application.</span></span> 
  
<span data-ttu-id="24d39-165">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-165">Schema format:</span></span>
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a><span data-ttu-id="24d39-166">Protocolo de retorno (opcional)</span><span class="sxs-lookup"><span data-stu-id="24d39-166">Passback protocol (optional)</span></span>

<span data-ttu-id="24d39-p109">Si desea que Office devuelva a los usuarios a su aplicación de iOS cuando elijan la flecha atrás, la aplicación que realizó la invocación deberá usar el protocolo de retorno, que incluye el descriptor "|p|" seguido del protocolo de la aplicación (sin los dos puntos). Deberá asegurarse de que la aplicación pueda gestionar correctamente la respuesta de Office.</span><span class="sxs-lookup"><span data-stu-id="24d39-p109">If you want Office to return users to your iOS application when they choose the back arrow, the invoking application will need to use the passback protocol, which includes the descriptor '|p|' followed by the app protocol (without a colon). You'll need to ensure that your application can properly handle the response from Office.</span></span>
  
<span data-ttu-id="24d39-169">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-169">Schema format:</span></span>
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a><span data-ttu-id="24d39-170">Contexto del documento (opcional)</span><span class="sxs-lookup"><span data-stu-id="24d39-170">Document context (optional)</span></span>

<span data-ttu-id="24d39-p110">Office no usa el contexto del documento, pero la aplicación de referencia podría necesitarlo cuando Office devuelve a un usuario. Si desea que el contexto del documento se devuelva con la aplicación, use el descriptor '|c|' seguido del contexto que desea como una cadena. Office no limita la longitud de la cadena más allá de los límites que imponga el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="24d39-p110">Office doesn't use the document context, but the referring application might need it when Office passes a user back. If you want the document context to be returned to your application, use the descriptor '|c|' followed by the context that you want as a string. Office does not limit the length of the string, beyond any limits imposed by the operating system.</span></span>
  
<span data-ttu-id="24d39-174">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-174">Schema format:</span></span>
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a><span data-ttu-id="24d39-175">Devolver a los usuarios a la aplicación de referencia</span><span class="sxs-lookup"><span data-stu-id="24d39-175">Return users to the referring application</span></span>

<span data-ttu-id="24d39-p111">Por motivos de seguridad, Office solo devuelve a los usuarios a la aplicación de referencia si el archivo se abrió correctamente. Cuando el usuario elige la flecha atrás, Office responde a la aplicación que realiza la invocación con el protocolo de retorno, el modo de apertura, la dirección URL, el estado de carga pendiente y el contexto del documento. El estado de carga pendiente usa el descriptor |z|, y el valor es sí o no.</span><span class="sxs-lookup"><span data-stu-id="24d39-p111">For security reasons, Office only returns users to the referring application if the file opened successfully. When the user chooses the back arrow, Office responds to the invoking application with the passback protocol, open mode, URL, upload pending status, and document context. The upload pending status uses the descriptor |z|, and is either yes or no.</span></span>
  
<span data-ttu-id="24d39-179">Formato de esquema:</span><span class="sxs-lookup"><span data-stu-id="24d39-179">Schema format:</span></span>
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a><span data-ttu-id="24d39-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="24d39-180">See also</span></span>
<span data-ttu-id="24d39-181"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="24d39-181"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="24d39-182">Método canOpenURL</span><span class="sxs-lookup"><span data-stu-id="24d39-182">canOpenURL method</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="24d39-183">Clase UIApplication</span><span class="sxs-lookup"><span data-stu-id="24d39-183">UIApplication class</span></span>](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [<span data-ttu-id="24d39-184">Objeto SKProductViewController</span><span class="sxs-lookup"><span data-stu-id="24d39-184">SKProductViewController object</span></span>](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

