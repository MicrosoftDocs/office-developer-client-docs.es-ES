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
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439096"
---
# <a name="openstreamonfile"></a><span data-ttu-id="d7025-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="d7025-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="d7025-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7025-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7025-105">Asigna e inicializa un objeto OLE **IStream** para tener acceso al contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="d7025-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="d7025-106">Esta función toma una cadena ANSI como nombre de archivo, incluida la ruta de acceso y la extensión de archivo; por lo tanto, se recomienda el uso de la versión Unicode de esta función, [OpenStreamOnFileW.](openstreamonfilew.md)</span><span class="sxs-lookup"><span data-stu-id="d7025-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7025-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d7025-107">Header file:</span></span>  <br/> |<span data-ttu-id="d7025-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d7025-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7025-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d7025-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7025-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7025-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7025-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d7025-111">Called by:</span></span>  <br/> |<span data-ttu-id="d7025-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d7025-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d7025-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7025-113">Parameters</span></span>

 <span data-ttu-id="d7025-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d7025-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d7025-115">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="d7025-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="d7025-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="d7025-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d7025-117">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="d7025-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="d7025-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7025-118">_ulFlags_</span></span>
  
> <span data-ttu-id="d7025-119">[entrada] Máscara de bits de marcas usadas para controlar la creación o apertura del archivo al que se debe tener acceso a través del objeto **OLE IStream** .</span><span class="sxs-lookup"><span data-stu-id="d7025-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="d7025-120">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="d7025-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="d7025-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="d7025-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="d7025-122">Se creará un archivo temporal para el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="d7025-123">Si se establece esta marca, también STGM_CREATE y STGM_READWRITE marca.</span><span class="sxs-lookup"><span data-stu-id="d7025-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="d7025-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="d7025-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="d7025-125">El archivo se creará incluso si ya existe uno.</span><span class="sxs-lookup"><span data-stu-id="d7025-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="d7025-126">Si no se establece el parámetro  _lpszFileName,_ se deben establecer tanto esta marca STGM_DELETEONRELEASE como el parámetro.</span><span class="sxs-lookup"><span data-stu-id="d7025-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="d7025-127">Si STGM_CREATE se establece, también STGM_READWRITE debe establecerse la marca de STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="d7025-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="d7025-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="d7025-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="d7025-129">El archivo se eliminará cuando se libera el objeto **IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="d7025-130">Si no se establece el parámetro  _lpszFileName,_ se deben establecer tanto esta marca STGM_CREATE como el parámetro.</span><span class="sxs-lookup"><span data-stu-id="d7025-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="d7025-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="d7025-131">STGM_READ</span></span> 
  
> <span data-ttu-id="d7025-132">El archivo se va a crear o abrir con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7025-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="d7025-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="d7025-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="d7025-134">El archivo se va a crear o abrir con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d7025-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="d7025-135">Si no se establece esta marca, la STGM_CREATE no debe establecerse.</span><span class="sxs-lookup"><span data-stu-id="d7025-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="d7025-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="d7025-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="d7025-137">[entrada] Nombre de archivo, incluida la ruta de acceso y la extensión, del archivo para el que **OpenStreamOnFile** inicializa el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="d7025-138">Si se SOF_UNIQUEFILENAME marca,  _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="d7025-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="d7025-139">Si  _lpszFileName_ es NULL, **OpenStreamOnFile** obtiene una ruta de acceso adecuada del sistema y se deben establecer las marcas STGM_CREATE y STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="d7025-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="d7025-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="d7025-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="d7025-141">[entrada] Prefijo del nombre de archivo en el que **OpenStreamOnFile** inicializa el **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="d7025-142">Si se establece, el prefijo no debe contener más de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="d7025-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="d7025-143">Si  _lpszPrefix_ es NULL, se usa un prefijo de "SOF".</span><span class="sxs-lookup"><span data-stu-id="d7025-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="d7025-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="d7025-144">_lppStream_</span></span>
  
> <span data-ttu-id="d7025-145">[salida] Puntero a un puntero a un objeto que expone la **interfaz IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7025-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7025-146">Return value</span></span>

<span data-ttu-id="d7025-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7025-147">S_OK</span></span> 
  
> <span data-ttu-id="d7025-148">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d7025-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d7025-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d7025-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d7025-150">No se pudo tener acceso al archivo debido a que los permisos de usuario no son suficientes o porque no se pueden modificar los archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7025-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="d7025-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d7025-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d7025-152">El archivo designado no existe.</span><span class="sxs-lookup"><span data-stu-id="d7025-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7025-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7025-153">Remarks</span></span>

<span data-ttu-id="d7025-154">La **función OpenStreamOnFile** tiene dos usos importantes, que se distinguen por la configuración de SOF_UNIQUEFILENAME marca.</span><span class="sxs-lookup"><span data-stu-id="d7025-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="d7025-155">Cuando no se establece esta marca, **OpenStreamOnFile** abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un archivo adjunto mediante el método **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="d7025-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="d7025-156">En este caso,  _el parámetro lpszFileName_ especifica la ruta de acceso y el nombre de archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="d7025-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="d7025-157">Cuando SOF_UNIQUEFILENAME se establece, **OpenStreamOnFile** crea un archivo temporal para contener los datos de un **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="d7025-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="d7025-158">Para este uso, el parámetro  _lpszFileName_ puede designar opcionalmente la ruta de acceso al directorio donde se va a crear el archivo y el parámetro  _lpszPrefix_ puede especificar opcionalmente un prefijo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d7025-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="d7025-159">Cuando la aplicación cliente de llamada o el proveedor de servicios termine con el objeto **IStream,** debe liberarlo llamando al método OLE **IStream::Release.**</span><span class="sxs-lookup"><span data-stu-id="d7025-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="d7025-160">MAPI usa las funciones a las que  _apuntan lpAllocateBuffer_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="d7025-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7025-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d7025-161">Notes to callers</span></span>

<span data-ttu-id="d7025-162">La SOF_UNIQUEFILENAME se usa para crear un archivo temporal con un nombre único para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d7025-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="d7025-163">Si se establece esta marca, el parámetro  _lpszFileName_ especifica la ruta de acceso para el archivo temporal y el parámetro  _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d7025-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="d7025-164">El nombre de archivo construido es <prefix> HHHH. TMP, donde HHHH es un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="d7025-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="d7025-165">Si  _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve de la función de Windows **GetTempPath** o en el directorio actual si no se ha designado ningún directorio de archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="d7025-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="d7025-166">Si no se SOF_UNIQUEFILENAME marca, se omite  _lpszPrefix_ y  _lpszFileName_ debe contener la ruta de acceso completa y el nombre de archivo del archivo que se va a abrir o crear.</span><span class="sxs-lookup"><span data-stu-id="d7025-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="d7025-167">El archivo se abrirá o creará en función de las demás marcas establecidas en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d7025-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7025-168">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d7025-168">MFCMAPI reference</span></span>

<span data-ttu-id="d7025-169">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d7025-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7025-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d7025-170">**File**</span></span>|<span data-ttu-id="d7025-171">**Función**</span><span class="sxs-lookup"><span data-stu-id="d7025-171">**Function**</span></span>|<span data-ttu-id="d7025-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d7025-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7025-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="d7025-173">File.cpp</span></span>  <br/> |<span data-ttu-id="d7025-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="d7025-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="d7025-175">MFCMAPI usa el **método OpenStreamOnFile** para abrir una secuencia en un archivo para que se puedan escribir datos adjuntos en él.</span><span class="sxs-lookup"><span data-stu-id="d7025-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7025-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7025-176">See also</span></span>



[<span data-ttu-id="d7025-177">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d7025-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

