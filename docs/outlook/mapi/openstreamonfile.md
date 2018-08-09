---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8c246968dcac719a8ee8177e20e802f9c7033435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818455"
---
# <a name="openstreamonfile"></a><span data-ttu-id="c53f0-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="c53f0-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="c53f0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c53f0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c53f0-105">Asigna e inicializa un objeto **IStream** OLE para tener acceso al contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c53f0-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="c53f0-106">Esta función toma una cadena ANSI como el nombre de archivo, incluida la ruta de acceso y la extensión de archivo, por lo tanto, uso de la versión de Unicode de esta función, [OpenStreamOnFileW](openstreamonfilew.md), se recomienda.</span><span class="sxs-lookup"><span data-stu-id="c53f0-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c53f0-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c53f0-107">Header file:</span></span>  <br/> |<span data-ttu-id="c53f0-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c53f0-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c53f0-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c53f0-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c53f0-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c53f0-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c53f0-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c53f0-111">Called by:</span></span>  <br/> |<span data-ttu-id="c53f0-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c53f0-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="c53f0-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c53f0-113">Parameters</span></span>

 <span data-ttu-id="c53f0-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c53f0-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c53f0-115">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="c53f0-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c53f0-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c53f0-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c53f0-117">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="c53f0-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c53f0-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c53f0-118">_ulFlags_</span></span>
  
> <span data-ttu-id="c53f0-119">[entrada] Máscara de bits de indicadores que se utilizan para controlar la creación o apertura del archivo para tener acceso a través del objeto **IStream** OLE.</span><span class="sxs-lookup"><span data-stu-id="c53f0-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="c53f0-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c53f0-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="c53f0-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="c53f0-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="c53f0-122">Es un archivo temporal que se creará para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="c53f0-123">Si se establece este marcador, también se deben establecer los indicadores STGM_CREATE y STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c53f0-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="c53f0-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="c53f0-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="c53f0-125">Es el archivo que se creará, incluso si ya existe una.</span><span class="sxs-lookup"><span data-stu-id="c53f0-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="c53f0-126">Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="c53f0-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="c53f0-127">Si se establece STGM_CREATE, también se debe establecer la marca STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c53f0-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="c53f0-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="c53f0-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="c53f0-129">Es el archivo que se eliminará cuando se libera el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="c53f0-130">Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c53f0-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="c53f0-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="c53f0-131">STGM_READ</span></span> 
  
> <span data-ttu-id="c53f0-132">El archivo es que se creen o se abrió con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c53f0-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="c53f0-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="c53f0-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="c53f0-134">Es el archivo que se creó o se abran con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c53f0-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="c53f0-135">Si no se establece este indicador, el indicador STGM_CREATE no debe establecerse cualquiera.</span><span class="sxs-lookup"><span data-stu-id="c53f0-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="c53f0-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="c53f0-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="c53f0-137">[entrada] El nombre de archivo, incluida la ruta de acceso y la extensión del archivo para el que **OpenStreamOnFile** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="c53f0-138">Si se establece la marca SOF_UNIQUEFILENAME, _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="c53f0-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="c53f0-139">Si _lpszFileName_ es NULL, **OpenStreamOnFile** Obtiene una ruta de acceso apropiado desde el sistema y se deben establecer el STGM_CREATE y la STGM_DELETEONRELEASE marcas.</span><span class="sxs-lookup"><span data-stu-id="c53f0-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="c53f0-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="c53f0-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="c53f0-141">[entrada] El prefijo del nombre de archivo en el que **OpenStreamOnFile** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="c53f0-142">Si se establece, el prefijo debe contener no más de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="c53f0-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="c53f0-143">Si _lpszPrefix_ es NULL, se utiliza un prefijo de "SOF".</span><span class="sxs-lookup"><span data-stu-id="c53f0-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="c53f0-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="c53f0-144">_lppStream_</span></span>
  
> <span data-ttu-id="c53f0-145">[out] Puntero a un puntero a un objeto que expone la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c53f0-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c53f0-146">Return value</span></span>

<span data-ttu-id="c53f0-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="c53f0-147">S_OK</span></span> 
  
> <span data-ttu-id="c53f0-148">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c53f0-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c53f0-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c53f0-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c53f0-150">No se pudo tener acceso el archivo debido a los permisos de usuario suficientes o debido a que no se pueden modificar los archivos de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c53f0-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="c53f0-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c53f0-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c53f0-152">No existe el archivo designado.</span><span class="sxs-lookup"><span data-stu-id="c53f0-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c53f0-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c53f0-153">Remarks</span></span>

<span data-ttu-id="c53f0-154">La función **OpenStreamOnFile** tiene dos usos importantes, diferenciados por la configuración de la marca SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="c53f0-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="c53f0-155">Cuando no se establece este marcador, **OpenStreamOnFile** se abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de los datos adjuntos con el **IStream :: CopyTo** (método).</span><span class="sxs-lookup"><span data-stu-id="c53f0-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="c53f0-156">En este caso, el parámetro _lpszFileName_ especifica la ruta de acceso y el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="c53f0-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="c53f0-157">Cuando se establece SOF_UNIQUEFILENAME, **OpenStreamOnFile** crea un archivo temporal para contener datos para un objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="c53f0-158">Para este uso, el parámetro _lpszFileName_ , opcionalmente, puede designar la ruta de acceso al directorio donde es el archivo que se creará y el parámetro _lpszPrefix_ , opcionalmente, puede especificar un prefijo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c53f0-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="c53f0-159">Cuando finalice la aplicación cliente que llama o el proveedor de servicios con el objeto **IStream** , que debe liberar llamando al método OLE **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c53f0-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="c53f0-160">MAPI utiliza las funciones que señala _lpAllocateBuffer_ y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="c53f0-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c53f0-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c53f0-161">Notes to callers</span></span>

<span data-ttu-id="c53f0-162">El indicador SOF_UNIQUEFILENAME se utiliza para crear un archivo temporal con un nombre único para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c53f0-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="c53f0-163">Si se establece este indicador, el _lpszFileName_ parámetro especifica la ruta de acceso para el archivo temporal y el parámetro _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c53f0-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="c53f0-164">Es el nombre de archivo construido <prefix>HHHH. TMP, donde HHHH es un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="c53f0-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="c53f0-165">Si _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve desde la función de Windows **GetTempPath**o el directorio actual si no se ha designado ningún directorio de archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="c53f0-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="c53f0-166">Si no está establecido el indicador SOF_UNIQUEFILENAME, se omite _lpszPrefix_ y _lpszFileName_ debe contener la ruta de acceso completa y el nombre del archivo que se va a abrir o crear.</span><span class="sxs-lookup"><span data-stu-id="c53f0-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="c53f0-167">El archivo se va a abrir o crear en función de los otros marcadores que se establecen en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c53f0-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c53f0-168">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c53f0-168">MFCMAPI reference</span></span>

<span data-ttu-id="c53f0-169">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c53f0-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c53f0-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c53f0-170">**File**</span></span>|<span data-ttu-id="c53f0-171">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="c53f0-171">**Function**</span></span>|<span data-ttu-id="c53f0-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c53f0-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c53f0-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="c53f0-173">File.cpp</span></span>  <br/> |<span data-ttu-id="c53f0-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="c53f0-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="c53f0-175">MFCMAPI usa el método **OpenStreamOnFile** para abrir un objeto stream en un archivo, por lo que se puede escribir un archivo adjunto a ella.</span><span class="sxs-lookup"><span data-stu-id="c53f0-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c53f0-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="c53f0-176">See also</span></span>



[<span data-ttu-id="c53f0-177">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c53f0-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

